
%% #manim-arc %%

![[Callouts#^manim-source-ref]]

## Docstring

```python
r"""Mobjects that are curved.

Examples
--------
.. manim:: UsefulAnnotations
    :save_last_frame:

    class UsefulAnnotations(Scene):
        def construct(self):
            m0 = Dot()
            m1 = AnnotationDot()
            m2 = LabeledDot("ii")
            m3 = LabeledDot(MathTex(r"\alpha").set_color(ORANGE))
            m4 = CurvedArrow(2*LEFT, 2*RIGHT, radius= -5)
            m5 = CurvedArrow(2*LEFT, 2*RIGHT, radius= 8)
            m6 = CurvedDoubleArrow(ORIGIN, 2*RIGHT)

            self.add(m0, m1, m2, m3, m4, m5, m6)
            for i, mobj in enumerate(self.mobjects):
                mobj.shift(DOWN * (i-3))

"""
```

## Module Imports

```python
from __future__ import annotations

__all__ = [
    "TipableVMobject",
    "Arc",
    "ArcBetweenPoints",
    "CurvedArrow",
    "CurvedDoubleArrow",
    "Circle",
    "Dot",
    "AnnotationDot",
    "LabeledDot",
    "Ellipse",
    "AnnularSector",
    "Sector",
    "Annulus",
    "CubicBezier",
    "ArcPolygon",
    "ArcPolygonFromArcs",
]

import itertools
import warnings
from typing import TYPE_CHECKING

import numpy as np
from typing_extensions import Self

from manim.constants import *
from manim.mobject.opengl.opengl_compatibility import ConvertToOpenGL
from manim.mobject.types.vectorized_mobject import VGroup, VMobject
from manim.utils.color import BLACK, BLUE, RED, WHITE, ParsableManimColor
from manim.utils.iterables import adjacent_pairs
from manim.utils.space_ops import (
    angle_of_vector,
    cartesian_to_spherical,
    line_intersection,
    perpendicular_bisector,
    rotate_vector,
)

if TYPE_CHECKING:
    import manim.mobject.geometry.tips as tips
    from manim.mobject.mobject import Mobject
    from manim.mobject.text.tex_mobject import SingleStringMathTex, Tex
    from manim.mobject.text.text_mobject import Text
    from manim.typing import (
        CubicBezierPoints,
        Point3D,
        QuadraticBezierPoints,
        Vector3D
    )
```


