
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

### SCENE_NOT_FOUND_MESSAGE

```python
# Messages
SCENE_NOT_FOUND_MESSAGE: str = """
   {} is not in the script
"""
```

### CHOOSE_NUMBER_MESSAGE

```python
CHOOSE_NUMBER_MESSAGE: str = """
Choose number corresponding to desired scene/arguments.
(Use comma separated list for multiple entries)
Choice(s): """
```

### INVALID_NUMBER_MESSAGE

```python
INVALID_NUMBER_MESSAGE: str = "Invalid scene numbers have been specified. Aborting."
```

### NO_SCENE_MESSAGE

```python
NO_SCENE_MESSAGE: str = """
   There are no scenes inside that module
"""
```

## Pango related

### NORMAL

```python
# Pango stuff
NORMAL: str = "NORMAL"
```

### ITALIC

```python
ITALIC: str = "ITALIC"
```
^manim-constant-pango-italic

### OBLIQUE

```python
OBLIQUE: str = "OBLIQUE"
```

### BOLD

```python
BOLD: str = "BOLD"
```

### THIN

```python
# Only for Pango from below
THIN: str = "THIN"
```

### ULTRALIGHT

```python
ULTRALIGHT: str = "ULTRALIGHT"
```

### LIGHT

```python
LIGHT: str = "LIGHT"
```

### SEMILIGHT

```python
SEMILIGHT: str = "SEMILIGHT"
```

### BOOK

```python
BOOK: str = "BOOK"
```

### MEDIUM

```python
MEDIUM: str = "MEDIUM"
```

### SEMIBOLD

```python
SEMIBOLD: str = "SEMIBOLD"
```

### ULTRABOLD

```python
ULTRABOLD: str = "ULTRABOLD"
```

### HEAVY

```python
HEAVY: str = "HEAVY"
```

### ULTRAHEAVY

```python
ULTRAHEAVY: str = "ULTRAHEAVY"
```

### RESAMPLING_ALGORITHMS

```python
RESAMPLING_ALGORITHMS: dict[str, any] = {
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

#### nearest

```python
RESAMPLING_ALGORITHMS["nearest"] = Resampling.NEAREST
```

#### none

```python
RESAMPLING_ALGORITHMS["none"] = Resampling.NEAREST
```

#### lanczos

```python
RESAMPLING_ALGORITHMS["lanczos"] = Resampling.LANCZOS
```

#### antialias

```python
RESAMPLING_ALGORITHMS["antialias"] = Resampling.LANCZOS
```

#### bilinear

```python
RESAMPLING_ALGORITHMS["bilinear"] = Resampling.BILINEAR
```

#### linear

```python
RESAMPLING_ALGORITHMS["nearest"] = Resampling.BILINEAR
```

#### bicubic

```python
RESAMPLING_ALGORITHMS["bicubic"] = Resampling.BICUBIC
```

#### cubic

```python
RESAMPLING_ALGORITHMS["cubic"] = Resampling.BICUBIC
```

#### box

```python
RESAMPLING_ALGORITHMS["box"] = Resampling.BOX
```

#### hamming

```python
RESAMPLING_ALGORITHMS["hamming"] = Resampling.HAMMING
```

## Geometry

### START_X

```python
# Geometry
START_X: int = 30
```

Type: [[Manim Dependencies/python3.12.4/Include/cpython/floatobject.h|float]]

### START_Y

```python
START_Y: int = 20
```

Type: [[Manim Dependencies/python3.12.4/Include/cpython/floatobject.h|float]]

### DEFAULT_DOT_RADIUS

```python
DEFAULT_DOT_RADIUS: float = 0.08
```

Type: [[Manim Dependencies/python3.12.4/Include/cpython/floatobject.h|float]]

### DEFAULT_SMALL_DOT_RADIUS

```python
DEFAULT_SMALL_DOT_RADIUS: float = 0.04
```

Type: [[Manim Dependencies/python3.12.4/Include/cpython/floatobject.h|float]]

### DEFAULT_DASH_LENGTH

```python
DEFAULT_DASH_LENGTH: float = 0.05
```

Type: [[Manim Dependencies/python3.12.4/Include/cpython/floatobject.h|float]]

### DEFAULT_ARROW_TIP_LENGTH

```python
DEFAULT_ARROW_TIP_LENGTH: float = 0.35
```

Type: [[Manim Dependencies/python3.12.4/Include/cpython/floatobject.h|float]]

### Directions

#### ORIGIN

```python
# Geometry: directions
ORIGIN: Vector3D = np.array((0.0, 0.0, 0.0))
"""The center of the coordinate system."""
```

Type: [[__vectors#Vector3D|Vector3D]]

#### UP

```python
UP: Vector3D = np.array((0.0, 1.0, 0.0))
"""One unit step in the positive Y direction."""
```

Type: [[__vectors#Vector3D|Vector3D]]

#### DOWN

```python
DOWN: Vector3D = np.array((0.0, -1.0, 0.0))
"""One unit step in the negative Y direction."""
```

Type: [[__vectors#Vector3D|Vector3D]]

#### RIGHT

```python
RIGHT: Vector3D = np.array((1.0, 0.0, 0.0))
"""One unit step in the positive X direction."""
```

Type: [[__vectors#Vector3D|Vector3D]]

#### LEFT

```python
LEFT: Vector3D = np.array((-1.0, 0.0, 0.0))
"""One unit step in the negative X direction."""
```

Type: [[__vectors#Vector3D|Vector3D]]

#### IN

```python
IN: Vector3D = np.array((0.0, 0.0, -1.0))
"""One unit step in the negative Z direction."""
```

Type: [[__vectors#Vector3D|Vector3D]]

#### OUT

```python
OUT: Vector3D = np.array((0.0, 0.0, 1.0))
"""One unit step in the positive Z direction."""
```

Type: [[__vectors#Vector3D|Vector3D]]

#### Diagonal Abbreviations

##### UL

```python
# Geometry: useful abbreviations for diagonals
UL: Vector3D = UP + LEFT
"""One step up plus one step left."""
```

Type: [[__vectors#Vector3D|Vector3D]]

##### UR

```python
UR: Vector3D = UP + RIGHT
"""One step up plus one step right."""
```

Type: [[__vectors#Vector3D|Vector3D]]

##### UR

```python
DL: Vector3D = DOWN + LEFT
"""One step down plus one step left."""
```

Type: [[__vectors#Vector3D|Vector3D]]

##### DR

```python
DR: Vector3D = DOWN + RIGHT
"""One step down plus one step right."""
```

Type: [[__vectors#Vector3D|Vector3D]]

### Axes

#### X_AXIS

```python
# Geometry: axes
X_AXIS: Vector3D = np.array((1.0, 0.0, 0.0))
```

Type: [[__vectors#Vector3D|Vector3D]]

#### Y_AXIS

```python
Y_AXIS: Vector3D = np.array((0.0, 1.0, 0.0))
```

Type: [[__vectors#Vector3D|Vector3D]]

#### Z_AXIS

```python
Z_AXIS: Vector3D = np.array((0.0, 0.0, 1.0))
```

Type: [[__vectors#Vector3D|Vector3D]]

## Default Buffers (Padding)

### SMALL_BUFF

```python
# Default buffers (padding)
SMALL_BUFF: float = 0.1
```

Type: [[__vectors#Vector3D|Vector3D]]

### MED_SMALL_BUFF

```python
MED_SMALL_BUFF = 0.25
```

Type: [[__vectors#Vector3D|Vector3D]]

### MED_LARGE_BUFF

```python
MED_LARGE_BUFF = 0.5
```

Type: [[__vectors#Vector3D|Vector3D]]

### LARGE_BUFF

```python
LARGE_BUFF = 1
```

Type: [[__vectors#Vector3D|Vector3D]]

### DEFAULT_MOBJECT_TO_EDGE_BUFFER

```python
DEFAULT_MOBJECT_TO_EDGE_BUFFER = MED_LARGE_BUFF
```

### DEFAULT_MOBJECT_TO_MOBJECT_BUFFER

```python
DEFAULT_MOBJECT_TO_MOBJECT_BUFFER = MED_SMALL_BUFF
```

### SMALL_BUFF

## Timings

> [!note]+
> The timings are in seconds

### DEFAULT_POINTWISE_FUNCTION_RUN_TIME

```python
# Times in seconds
DEFAULT_POINTWISE_FUNCTION_RUN_TIME = 3.0 # seconds
```

### DEFAULT_WAIT_TIME

```python
DEFAULT_WAIT_TIME = 1.0 # second
```

## Mathematic

### PI

```python
# Mathematical constants
PI = np.pi
"""The ratio of the circumference of a circle to its diameter."""
```

### TAU

```python
TAU = 2 * PI
"""The ratio of the circumference of a circle to its radius."""
```

### DEGREES

```python
DEGREES = TAU / 360
"""The exchange rate between radians and degrees."""
```

## Video Quality Values

### QUALITIES

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

### DEFAULT_QUALITY

```python
DEFAULT_QUALITY = "high_quality"
```

## Misc

### DEFAULT_POINT_DENSITY_2D

```python
# Misc
DEFAULT_POINT_DENSITY_2D = 25
```

### DEFAULT_POINT_DENSITY_1D

```python
DEFAULT_POINT_DENSITY_1D = 10
```

### DEFAULT_STROKE_WIDTH

```python
DEFAULT_STROKE_WIDTH = 4
```

### DEFAULT_FONT_SIZE

```python
DEFAULT_FONT_SIZE = 48
```

### SCALE_FACTOR_PER_FONT_POINT

```python
SCALE_FACTOR_PER_FONT_POINT = 1 / 960
```

### EPILOG

```python
EPILOG = "Made with <3 by Manim Community developers."
```

### SHIFT_VALUE

```python
SHIFT_VALUE = 65505
```

### CTRL_VALUE

```python
CTRL_VALUE = 65507
```

### CONTEXT_SETTINGS

```python
CONTEXT_SETTINGS = Context.settings(
    align_option_groups=True,
    align_sections=True,
    show_constraints=True,
)
```

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

#### CAIRO

```python
CAIRO = "cairo"  #: A renderer based on the cairo backend.
```

#### OPENGL

```python
OPENGL = "opengl"  #: An OpenGL-based renderer.
```

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

#### AUTO

```python
AUTO = 0
```

#### ROUND

```python
ROUND = 1
```

#### BEVEL

```python
BEVEL = 2
```

#### MITER

```python
MITER = 3
```

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

#### CapStyleType.AUTO

```python
CapStyleType.AUTO = 0
```

#### CapStyleType.ROUND

```python
CapStyleType.ROUND = 1
```

#### CapStyleType.BUTT

```python
CapStyleType.BUTT = 2
```

#### CapStyleType.SQUARE

```python
CapStyleType.SQUARE = 3
```

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

