
![[Callouts#^manim-source-ref]]

## Docstring

```python
"""
Constant definitions.
"""
```

## Module Imports

```python
from __future__ import annotations

from enum import Enum

import numpy as np
from cloup import Context
from PIL.Image import Resampling

from manim.typing import Vector3D
```
## Module Exports

### All

```python
__all__ = [
    "SCENE_NOT_FOUND_MESSAGE",
    "CHOOSE_NUMBER_MESSAGE",
    "INVALID_NUMBER_MESSAGE",
    "NO_SCENE_MESSAGE",
    "NORMAL",
    "ITALIC",
    "OBLIQUE",
    "BOLD",
    "THIN",
    "ULTRALIGHT",
    "LIGHT",
    "SEMILIGHT",
    "BOOK",
    "MEDIUM",
    "SEMIBOLD",
    "ULTRABOLD",
    "HEAVY",
    "ULTRAHEAVY",
    "RESAMPLING_ALGORITHMS",
    "ORIGIN",
    "UP",
    "DOWN",
    "RIGHT",
    "LEFT",
    "IN",
    "OUT",
    "X_AXIS",
    "Y_AXIS",
    "Z_AXIS",
    "UL",
    "UR",
    "DL",
    "DR",
    "START_X",
    "START_Y",
    "DEFAULT_DOT_RADIUS",
    "DEFAULT_SMALL_DOT_RADIUS",
    "DEFAULT_DASH_LENGTH",
    "DEFAULT_ARROW_TIP_LENGTH",
    "SMALL_BUFF",
    "MED_SMALL_BUFF",
    "MED_LARGE_BUFF",
    "LARGE_BUFF",
    "DEFAULT_MOBJECT_TO_EDGE_BUFFER",
    "DEFAULT_MOBJECT_TO_MOBJECT_BUFFER",
    "DEFAULT_POINTWISE_FUNCTION_RUN_TIME",
    "DEFAULT_WAIT_TIME",
    "DEFAULT_POINT_DENSITY_2D",
    "DEFAULT_POINT_DENSITY_1D",
    "DEFAULT_STROKE_WIDTH",
    "DEFAULT_FONT_SIZE",
    "SCALE_FACTOR_PER_FONT_POINT",
    "PI",
    "TAU",
    "DEGREES",
    "QUALITIES",
    "DEFAULT_QUALITY",
    "EPILOG",
    "CONTEXT_SETTINGS",
    "SHIFT_VALUE",
    "CTRL_VALUE",
    "RendererType",
    "LineJointType",
    "CapStyleType",
]
```
## Messages

```python
# Messages
SCENE_NOT_FOUND_MESSAGE = """
   {} is not in the script
"""
```
^manim-const-SceneNotFoundMessage

```python
CHOOSE_NUMBER_MESSAGE = """
Choose number corresponding to desired scene/arguments.
(Use comma separated list for multiple entries)
Choice(s): """
```
^manim-const-ChooseNumberMessage

```python
INVALID_NUMBER_MESSAGE = "Invalid scene numbers have been specified. Aborting."
```
^manim-const-ChooseNumberMessage

```python
NO_SCENE_MESSAGE = """
   There are no scenes inside that module
"""
```
^manim-const-NoSceneMessage

## Pango related

```python
# Pango stuff
NORMAL = "NORMAL"
```
^manim-constant-pango-normal

```python
ITALIC = "ITALIC"
```
^manim-constant-pango-italic

```python
OBLIQUE = "OBLIQUE"
```
^manim-constant-pango-oblique

```python
BOLD = "BOLD"
```
^manim-constant-pango-bold

```python
# Only for Pango from below
THIN = "THIN"
```
^manim-constant-pango-thin

```python
ULTRALIGHT = "ULTRALIGHT"
```
^manim-constant-pango-ultralight

```python
LIGHT = "LIGHT"
```
^manim-constant-pango-light

```python
SEMILIGHT = "SEMILIGHT"
```
^manim-constant-pango-semilight

```python
BOOK = "BOOK"
```
^manim-constant-pango-book

```python
MEDIUM = "MEDIUM"
```
^manim-constant-pango-medium

```python
SEMIBOLD = "SEMIBOLD"
```
^manim-constant-pango-semibold

```python
ULTRABOLD = "ULTRABOLD"
```
^manim-constant-pango-ultrabold

```python
HEAVY = "HEAVY"
```
^manim-constant-pango-heavy

```python
ULTRAHEAVY = "ULTRAHEAVY"
```
^manim-constant-pango-ultraheavy

```python
RESAMPLING_ALGORITHMS = {
    "nearest": Resampling.NEAREST,
    "none": Resampling.NEAREST,
    "lanczos": Resampling.LANCZOS,
    "antialias": Resampling.LANCZOS,
    "bilinear": Resampling.BILINEAR,
    "linear": Resampling.BILINEAR,
    "bicubic": Resampling.BICUBIC,
    "cubic": Resampling.BICUBIC,
    "box": Resampling.BOX,
    "hamming": Resampling.HAMMING,
}
```
^manim-constant-pango-resamplingalgorithms

## Geometry

```python
# Geometry
START_X = 30
```
^manim-const-startx

```python
START_Y = 20
```
^manim-const-starty

```python
DEFAULT_DOT_RADIUS = 0.08
```
^manim-const-DefaultDotRadius

```python
DEFAULT_SMALL_DOT_RADIUS = 0.04
```
^manim-const-DefaultSmallDotRadius

```python
DEFAULT_DASH_LENGTH = 0.05
```
^manim-const-DefaultDashLength

```python
DEFAULT_ARROW_TIP_LENGTH = 0.35
```
^manim-const-DefaultArrowTipLength

### Directions

```python
# Geometry: directions
ORIGIN: Vector3D = np.array((0.0, 0.0, 0.0))
"""The center of the coordinate system."""
```
^manim-const-origin

```python
UP: Vector3D = np.array((0.0, 1.0, 0.0))
"""One unit step in the positive Y direction."""
```
^manim-const-up

```python
DOWN: Vector3D = np.array((0.0, -1.0, 0.0))
"""One unit step in the negative Y direction."""
```
^manim-const-down

```python
RIGHT: Vector3D = np.array((1.0, 0.0, 0.0))
"""One unit step in the positive X direction."""
```
^manim-const-right

```python
LEFT: Vector3D = np.array((-1.0, 0.0, 0.0))
"""One unit step in the negative X direction."""
```
^manim-const-left

```python
IN: Vector3D = np.array((0.0, 0.0, -1.0))
"""One unit step in the negative Z direction."""
```
^manim-const-in

```python
OUT: Vector3D = np.array((0.0, 0.0, 1.0))
"""One unit step in the positive Z direction."""
```
^manim-const-out

#### Diagonal Abbreviations

```python
# Geometry: useful abbreviations for diagonals
UL: Vector3D = UP + LEFT
"""One step up plus one step left."""
```
^manim-const-ul

```python
UR: Vector3D = UP + RIGHT
"""One step up plus one step right."""
```
^manim-const-ur

```python
DL: Vector3D = DOWN + LEFT
"""One step down plus one step left."""
```
^manim-const-dl

```python
DR: Vector3D = DOWN + RIGHT
"""One step down plus one step right."""
```
^manim-const-dr

### Axes

```python
# Geometry: axes
X_AXIS: Vector3D = np.array((1.0, 0.0, 0.0))
```
^manim-const-xAxis

```python
Y_AXIS: Vector3D = np.array((0.0, 1.0, 0.0))
```
^manim-const-yAxis

```python
Z_AXIS: Vector3D = np.array((0.0, 0.0, 1.0))
```
^manim-const-zAxis

## Default Buffers (Padding)

```python
# Default buffers (padding)
SMALL_BUFF = 0.1
```
^manim-const-SmallBuff

```python
MED_SMALL_BUFF = 0.25
```
^manim-const-MedSmallBuff

```python
MED_LARGE_BUFF = 0.5
```
^manim-const-MedLargeBuff

```python
LARGE_BUFF = 1
```
^manim-const-LargeBuff

```python
DEFAULT_MOBJECT_TO_EDGE_BUFFER = MED_LARGE_BUFF
```
^manim-const-DefaultMobjectToEdgeBuffer

```python
DEFAULT_MOBJECT_TO_MOBJECT_BUFFER = MED_SMALL_BUFF
```
^manim-const-DefaultMobjectToMobjectBuffer

## Timings

> [!note]+
> The timings are in seconds

```python
# Times in seconds
DEFAULT_POINTWISE_FUNCTION_RUN_TIME = 3.0 # seconds
```
^manim-const-DefaultPointwiseFunctionRunTime

```python
DEFAULT_WAIT_TIME = 1.0 # second
```
^manim-const-DefaultWaitTIme

## Mathematic

```python
# Mathematical constants
PI = np.pi
"""The ratio of the circumference of a circle to its diameter."""
```
^manim-const-pi

```python
TAU = 2 * PI
"""The ratio of the circumference of a circle to its radius."""
```
^manim-const-tau

```python
DEGREES = TAU / 360
"""The exchange rate between radians and degrees."""
```
^manim-const-degrees

## Video Quality Values

```python
# Video qualities
QUALITIES: dict[str, dict[str, str | int | None]] = {
    "fourk_quality": {
        "flag": "k",
        "pixel_height": 2160,
        "pixel_width": 3840,
        "frame_rate": 60,
    },
    "production_quality": {
        "flag": "p",
        "pixel_height": 1440,
        "pixel_width": 2560,
        "frame_rate": 60,
    },
    "high_quality": {
        "flag": "h",
        "pixel_height": 1080,
        "pixel_width": 1920,
        "frame_rate": 60,
    },
    "medium_quality": {
        "flag": "m",
        "pixel_height": 720,
        "pixel_width": 1280,
        "frame_rate": 30,
    },
    "low_quality": {
        "flag": "l",
        "pixel_height": 480,
        "pixel_width": 854,
        "frame_rate": 15,
    },
    "example_quality": {
        "flag": None,
        "pixel_height": 480,
        "pixel_width": 854,
        "frame_rate": 30,
    },
}
```
^manim-const-qualities

```python
DEFAULT_QUALITY = "high_quality"
```
^manim-const-DefaultQuality

## Misc

```python
# Misc
DEFAULT_POINT_DENSITY_2D = 25
```
^manim-const-DefaultPointDensity2D

```python
DEFAULT_POINT_DENSITY_1D = 10
```
^manim-const-DefaultPointDensity1D

```python
DEFAULT_STROKE_WIDTH = 4
```
^manim-const-DefaultStrokeWidth

```python
DEFAULT_FONT_SIZE = 48
```
^manim-const-DefaultStrokeWidth

```python
SCALE_FACTOR_PER_FONT_POINT = 1 / 960
```
^manim-const-ScaleFactorPerFontPoint

```python
EPILOG = "Made with <3 by Manim Community developers."
```
^manim-const-epilog

```python
SHIFT_VALUE = 65505
```
^manim-const-ShiftValue

```python
CTRL_VALUE = 65507
```
^manim-const-CtrlValue

```python
CONTEXT_SETTINGS = Context.settings(
    align_option_groups=True,
    align_sections=True,
    show_constraints=True,
)
```
^manim-const-ContextSettings

## Enums

### RendererType

```python
class RendererType(Enum):
    """An enumeration of all renderer types that can be assigned to
    the ``config.renderer`` attribute.

    Manim's configuration allows assigning string values to the renderer
    setting, the values are then replaced by the corresponding enum object.
    In other words, you can run::

        config.renderer = "opengl"

    and checking the renderer afterwards reveals that the attribute has
    assumed the value::

        <RendererType.OPENGL: 'opengl'>
    """

    CAIRO = "cairo"  #: A renderer based on the cairo backend.
    OPENGL = "opengl"  #: An OpenGL-based renderer.
```

```python
CAIRO = "cairo"  #: A renderer based on the cairo backend.
```
^manim-const-RendererType-cairo

```python
OPENGL = "opengl"  #: An OpenGL-based renderer.
```
^manim-const-RendererType-cairo

### LineJointType

```python
class LineJointType(Enum):
    """Collection of available line joint types.

    See the example below for a visual illustration of the different
    joint types.

    Examples
    --------

    .. manim:: LineJointVariants
        :save_last_frame:

        class LineJointVariants(Scene):
            def construct(self):
                mob = VMobject(stroke_width=20, color=GREEN).set_points_as_corners([
                    np.array([-2, 0, 0]),
                    np.array([0, 0, 0]),
                    np.array([-2, 1, 0]),
                ])
                lines = VGroup(*[mob.copy() for _ in range(len(LineJointType))])
                for line, joint_type in zip(lines, LineJointType):
                    line.joint_type = joint_type

                lines.arrange(RIGHT, buff=1)
                self.add(lines)
                for line in lines:
                    label = Text(line.joint_type.name).next_to(line, DOWN)
                    self.add(label)
    """

    AUTO = 0
    ROUND = 1
    BEVEL = 2
    MITER = 3
```

```python
AUTO = 0
```
^manim-const-LineJointType-auto

```python
ROUND = 1
```
^manim-const-LineJointType-round

```python
BEVEL = 2
```
^manim-const-LineJointType-bevel

```python
MITER = 3
```
^manim-const-LineJointType-miter

#### Example

```python
class LineJointVariants(Scene):
    def construct(self):
        mob = VMobject(
            set_width=20,
            color=GREEN
        ).set_points_as_corners([
            np.array([-2, 0, 0]),
            np.array([ 0, 0, 0]),
            np.array([-2, 1, 0]),
        ])
        lines = VGroup(*[
            mob.copy() for _ in range(len(LineJointType))
        ])

        for line, joint_type in zip(lines, LineJointType):
            line.joint_type = joint_type

        lines.arrange(RIGHT, buff=1)
        self.add(lines)

        for line in lines:
            label = Text(line.joint_type.name).next_to(line, DOWN)
```

### CapStyleType

```python
class CapStyleType(Enum):
    """Collection of available cap styles.

    See the example below for a visual illustration of the different
    cap styles.

    Examples
    --------

    .. manim:: CapStyleVariants
        :save_last_frame:

        class CapStyleVariants(Scene):
            def construct(self):
                arcs = VGroup(*[
                    Arc(
                        radius=1,
                        start_angle=0,
                        angle=TAU / 4,
                        stroke_width=20,
                        color=GREEN,
                        cap_style=cap_style,
                    )
                    for cap_style in CapStyleType
                ])
                arcs.arrange(RIGHT, buff=1)
                self.add(arcs)
                for arc in arcs:
                    label = Text(arc.cap_style.name, font_size=24).next_to(arc, DOWN)
                    self.add(label)
    """

    AUTO = 0
    ROUND = 1
    BUTT = 2
    SQUARE = 3
```

```python
CapStyleType.AUTO = 0
```
^manim-const-CapStyleType-auto

```python
CapStyleType.ROUND = 1
```
^manim-const-CapStyleType-round

```python
CapStyleType.BUTT = 2
```
^manim-const-CapStyleType-butt

```python
CapStyleType.SQUARE = 3
```
^manim-const-CapStyleType-square

#### Example

```python
class CapStyleVariants(Scene):
    def construct(self):
        arcs = VGroup(*[
            Arc(
                radius=1,
                start_angle=0,
                angle=TAU / 4,
                stroke_width=20,
                color=GREEN,
                cap_style=cap_style
            )
            for cap_style in CapStyleType
        ])
        arcs.arrange(RIGHT, buff=1)
        self.add(arcs)
        for arc in arcs:
            label = Text(
                arc.cap_style_name,
                font_size=24
            ).next_to(arc, DOWN)
            self.add(label)
```

