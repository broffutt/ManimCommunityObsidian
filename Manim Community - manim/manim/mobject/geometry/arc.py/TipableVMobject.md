
%% #manim-arc %%

```python
class TipableVMobject(VMobject, metaclass=ConvertToOpenGL):
    """Meant for shared functionality between Arc and Line.
    Functionality can be classified broadly into these groups:

        * Adding, Creating, Modifying tips
            - add_tip calls create_tip, before pushing the new tip
                into the TipableVMobject's list of submobjects
            - stylistic and positional configuration

        * Checking for tips
            - Boolean checks for whether the TipableVMobject has a tip
                and a starting tip

        * Getters
            - Straightforward accessors, returning information pertaining
                to the TipableVMobject instance's tip(s), its length etc
    """

    def __init__(
        self,
        tip_length: float = DEFAULT_ARROW_TIP_LENGTH,
        normal_vector: Vector3D = OUT,
        tip_style: dict = {},
        **kwargs,
    ) -> None:
        self.tip_length: float = tip_length
        self.normal_vector: Vector3D = normal_vector
        self.tip_style: dict = tip_style
        super().__init__(**kwargs)

    # Adding, Creating, Modifying tips

    def add_tip(
        self,
        tip: tips.ArrowTip | None = None,
        tip_shape: type[tips.ArrowTip] | None = None,
        tip_length: float | None = None,
        tip_width: float | None = None,
        at_start: bool = False,
    ) -> Self:
        """Adds a tip to the TipableVMobject instance, recognising
        that the endpoints might need to be switched if it's
        a 'starting tip' or not.
        """
        if tip is None:
            tip = self.create_tip(tip_shape, tip_length, tip_width, at_start)
        else:
            self.position_tip(tip, at_start)
        self.reset_endpoints_based_on_tip(tip, at_start)
        self.asign_tip_attr(tip, at_start)
        self.add(tip)
        return self

    def create_tip(
        self,
        tip_shape: type[tips.ArrowTip] | None = None,
        tip_length: float = None,
        tip_width: float = None,
        at_start: bool = False,
    ):
        """Stylises the tip, positions it spatially, and returns
        the newly instantiated tip to the caller.
        """
        tip = self.get_unpositioned_tip(tip_shape, tip_length, tip_width)
        self.position_tip(tip, at_start)
        return tip

    def get_unpositioned_tip(
        self,
        tip_shape: type[tips.ArrowTip] | None = None,
        tip_length: float | None = None,
        tip_width: float | None = None,
    ):
        """Returns a tip that has been stylistically configured,
        but has not yet been given a position in space.
        """
        from manim.mobject.geometry.tips import ArrowTriangleFilledTip

        style = {}

        if tip_shape is None:
            tip_shape = ArrowTriangleFilledTip

        if tip_shape is ArrowTriangleFilledTip:
            if tip_width is None:
                tip_width = self.get_default_tip_length()
            style.update({"width": tip_width})
        if tip_length is None:
            tip_length = self.get_default_tip_length()

        color = self.get_color()
        style.update({"fill_color": color, "stroke_color": color})
        style.update(self.tip_style)
        tip = tip_shape(length=tip_length, **style)
        return tip

    def position_tip(self, tip: tips.ArrowTip, at_start: bool = False):
        # Last two control points, defining both
        # the end, and the tangency direction
        if at_start:
            anchor = self.get_start()
            handle = self.get_first_handle()
        else:
            handle = self.get_last_handle()
            anchor = self.get_end()
        angles = cartesian_to_spherical(handle - anchor)
        tip.rotate(
            angles[1] - PI - tip.tip_angle,
        )  # Rotates the tip along the azimuthal
        if not hasattr(self, "_init_positioning_axis"):
            axis = [
                np.sin(angles[1]),
                -np.cos(angles[1]),
                0,
            ]  # Obtains the perpendicular of the tip
            tip.rotate(
                -angles[2] + PI / 2,
                axis=axis,
            )  # Rotates the tip along the vertical wrt the axis
            self._init_positioning_axis = axis
        tip.shift(anchor - tip.tip_point)
        return tip

    def reset_endpoints_based_on_tip(self, tip: tips.ArrowTip, at_start: bool) -> Self:
        if self.get_length() == 0:
            # Zero length, put_start_and_end_on wouldn't work
            return self

        if at_start:
            self.put_start_and_end_on(tip.base, self.get_end())
        else:
            self.put_start_and_end_on(self.get_start(), tip.base)
        return self

    def asign_tip_attr(self, tip: tips.ArrowTip, at_start: bool) -> Self:
        if at_start:
            self.start_tip = tip
        else:
            self.tip = tip
        return self

    # Checking for tips

    def has_tip(self) -> bool:
        return hasattr(self, "tip") and self.tip in self

    def has_start_tip(self) -> bool:
        return hasattr(self, "start_tip") and self.start_tip in self

    # Getters

    def pop_tips(self) -> VGroup:
        start, end = self.get_start_and_end()
        result = self.get_group_class()()
        if self.has_tip():
            result.add(self.tip)
            self.remove(self.tip)
        if self.has_start_tip():
            result.add(self.start_tip)
            self.remove(self.start_tip)
        self.put_start_and_end_on(start, end)
        return result

    def get_tips(self) -> VGroup:
        """Returns a VGroup (collection of VMobjects) containing
        the TipableVMObject instance's tips.
        """
        result = self.get_group_class()()
        if hasattr(self, "tip"):
            result.add(self.tip)
        if hasattr(self, "start_tip"):
            result.add(self.start_tip)
        return result

    def get_tip(self):
        """Returns the TipableVMobject instance's (first) tip,
        otherwise throws an exception."""
        tips = self.get_tips()
        if len(tips) == 0:
            raise Exception("tip not found")
        else:
            return tips[0]

    def get_default_tip_length(self) -> float:
        return self.tip_length

    def get_first_handle(self) -> Point3D:
        return self.points[1]

    def get_last_handle(self) -> Point3D:
        return self.points[-2]

    def get_end(self) -> Point3D:
        if self.has_tip():
            return self.tip.get_start()
        else:
            return super().get_end()

    def get_start(self) -> Point3D:
        if self.has_start_tip():
            return self.start_tip.get_start()
        else:
            return super().get_start()

    def get_length(self) -> np.floating:
        start, end = self.get_start_and_end()
        return np.linalg.norm(start - end)
```
