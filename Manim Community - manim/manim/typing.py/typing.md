
%% #manim-typing %%

![[Callouts#^manim-source-ref]]

## Docstring

```python
"""Custom type definitions used in Manim.

.. admonition:: Note for developers
    :class: important

    Around the source code there are multiple strings which look like this:

    .. code-block::

        '''
        [CATEGORY]
        <category_name>
        '''

    All type aliases defined under those strings will be automatically
    classified under that category.

    If you need to define a new category, respect the format described above.
"""
```

This note is how the above `admonition` renders on the [[typing#^docsiteref|Docs Page]].

> [!important] Note for Developers
> Around the source code there are multiple strings which look like this:
> ```toml
> '''
> [CATEGORY]
> <category_name>
> '''
> ```
> All type aliases defined under those strings will be automatically
> classified under that category.
> 
> If you need to define a new category, respect the format described above.

## Module Imports

```python
from __future__ import annotations

from os import PathLike
from typing import Callable, Union

import numpy as np
import numpy.typing as npt
from typing_extensions import TypeAlias
```
## Module Exports

### All

```python
__all__ = [
    "ManimFloat",
    "ManimInt",
    "ManimColorDType",
    "RGB_Array_Float",
    "RGB_Tuple_Float",
    "RGB_Array_Int",
    "RGB_Tuple_Int",
    "RGBA_Array_Float",
    "RGBA_Tuple_Float",
    "RGBA_Array_Int",
    "RGBA_Tuple_Int",
    "HSV_Array_Float",
    "HSV_Tuple_Float",
    "ManimColorInternal",
    "PointDType",
    "InternalPoint2D",
    "Point2D",
    "InternalPoint2D_Array",
    "Point2D_Array",
    "InternalPoint3D",
    "Point3D",
    "InternalPoint3D_Array",
    "Point3D_Array",
    "Vector2D",
    "Vector2D_Array",
    "Vector3D",
    "Vector3D_Array",
    "VectorND",
    "VectorND_Array",
    "RowVector",
    "ColVector",
    "MatrixMN",
    "Zeros",
    "QuadraticBezierPoints",
    "QuadraticBezierPoints_Array",
    "QuadraticBezierPath",
    "QuadraticSpline",
    "CubicBezierPoints",
    "CubicBezierPoints_Array",
    "CubicBezierPath",
    "CubicSpline",
    "BezierPoints",
    "BezierPoints_Array",
    "BezierPath",
    "Spline",
    "FlatBezierPoints",
    "FunctionOverride",
    "PathFuncType",
    "MappingFunction",
    "Image",
    "GrayscaleImage",
    "RGBImage",
    "RGBAImage",
    "StrPath",
    "StrOrBytesPath",
]
```
## Type Aliases

#### Contents

> [!tip]+ Preview
> Hover over the items to preview its definition.\
> If in the editor, hover then press `CTRL`

- [[__primitives|Primitive Data Types]]
	- [[__primitives#ManimFloat|ManimFloat]]
	- [[__primitives#ManimInt|ManimInt]]
- [[__colors|Color Data Types]]
	- [[__colors#ManimColorDType|ManimColorDType]]
	- [[__colors#RGB_Array_Float|RGB_Array_Float]]
	- [[__colors#RGB_Tuple_Float|RGB_Tuple_Float]]
	- [[__colors#RGB_Array_Int|RGB_Array_Int]]
	- [[__colors#RGB_Tuple_Int|RGB_Tuple_Int]]
	- [[__colors#RGBA_Array_Float|RGBA_Array_Float]]
	- [[__colors#RGBA_Tuple_Float|RGBA_Tuple_Float]]
	- [[__colors#RGBA_Array_Int|RGBA_Array_Int]]
	- [[__colors#RGBA_Tuple_Int|RGBA_Tuple_Int]]
	- [[__colors#HSV_Array_Float|HSV_Array_Float]]
	- [[__colors#HSV_Tuple_Float|HSV_Tuple_Float]]
	- [[__colors#ManimColorInternal|ManimColorInternal]]
- [[__points|Point Data Types]]
	- [[__points#PointDType|PointDType]]
	- [[__points#InternalPoint2D|InternalPoint2D]]
	- [[__points#Point2D|Point2D]]
	- [[__points#InternalPoint2D_Array|InternalPoint2D_Array]]
	- [[__points#Point2D_Array|Point2D_Array]]
	- [[__points#InternalPoint3D|InternalPoint3D]]
	- [[__points#Point3D|Point3D]]
	- [[__points#InternalPoint3D_Array|InternalPoint3D_Array]]
	- [[__points#Point3D_Array|Point3D_Array]]
- [[__vectors|Vector Data Types]]
	- [[__vectors#Vector2D|Vector2D]]
	- [[__vectors#Vector2D_Array|Vector2D_Array]]
	- [[__vectors#Vector3D|Vector3D]]
	- [[__vectors#Vector3D_Array|Vector3D_Array]]
	- [[__vectors#Vector3D_Array|Vector3D_Array]]
	- [[__vectors#VectorND|VectorND]]
	- [[__vectors#VectorND_Array|VectorND_Array]]
	- [[__vectors#RowVector|RowVector]]
	- [[__vectors#ColVector|ColVector]]
- [[__matrices|Matrix Data Types]]
	- [[__matrices#MatrixMN|MatrixMN]]
	- [[__matrices#Zeros|Zeros]]
- [[__bézier|Bézier Data Types]]
    - [[__bézier#QuadraticBezierPoints|QuadraticBezierPoints]]
    - [[__bézier#QuadraticBezierPoints_Array|QuadraticBezierPoints_Array]]
    - [[__bézier#QuadraticBezierPath|QuadraticBezierPath]]
    - [[__bézier#QuadraticSpline|QuadraticSpline]]
    - [[__bézier#CubicBezierPoints|CubicBezierPoints]]
    - [[__bézier#CubicBezierPoints_Array|CubicBezierPoints_Array]]
    - [[__bézier#CubicBezierPath|CubicBezierPath]]
    - [[__bézier#CubicSpline|CubicSpline]]
    - [[__bézier#BezierPoints|BezierPoints]]
    - [[__bézier#BezierPoints_Array|BezierPoints_Array]]
    - [[__bézier#BezierPath|BezierPath]]
    - [[__bézier#Spline|Spline]]
    - [[__bézier#FlatBezierPoints|FlatBezierPoints]]
- [[__functions|Function Data Types]]
    - [[__functions#FunctionOverride|FunctionOverride]]
    - [[__functions#PathFuncType|PathFuncType]]
    - [[__functions#MappingFunction|MappingFunction]]
- [[__images|Image Data Types]]
    - [[__images#Image|Image]]
    - [[__images#GrayscaleImage|GrayscaleImage]]
    - [[__images#RGBImage|RGBImage]]
    - [[__images#RGBAImage|RGBAImage]]
- [[__paths|Path Data Types]]
    - [[__paths#StrPath|StrPath]]
    - [[__paths#StrOrBytesPath|StrOrBytesPath]]
