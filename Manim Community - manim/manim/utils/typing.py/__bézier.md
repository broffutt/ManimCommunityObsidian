
## Bézier Data Types

```python
"""
[CATEGORY]
Bézier types
"""
```

### QuadraticBezierPoints

```python
QuadraticBezierPoints: TypeAlias = Union[
    npt.NDArray[PointDType], tuple[Point3D, Point3D, Point3D]
]
"""``shape: (3, 3)``

A `Point3D_Array` of 3 control points for a single quadratic Bézier
curve:
``[[float, float, float], [float, float, float], [float, float, float]]``.
"""
```

### QuadraticBezierPoints_Array

```python
QuadraticBezierPoints_Array: TypeAlias = Union[
    npt.NDArray[PointDType], tuple[QuadraticBezierPoints, ...]
]
"""``shape: (N, 3, 3)``

An array of :math:`N` `QuadraticBezierPoints` objects:
``[[[float, float, float], [float, float, float], [float, float, float]], ...]``.
"""
```

### QuadraticBezierPath

```python
QuadraticBezierPath: TypeAlias = Point3D_Array
"""``shape: (3*N, 3)``

A `Point3D_Array` of :math:`3N` points, where each one of the
:math:`N` consecutive blocks of 3 points represents a quadratic
Bézier curve:
``[[float, float, float], ...], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### QuadraticSpline

```python
QuadraticSpline: TypeAlias = QuadraticBezierPath
"""``shape: (3*N, 3)``

A special case of `QuadraticBezierPath` where all the :math:`N`
quadratic Bézier curves are connected, forming a quadratic spline:
``[[float, float, float], ...], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### CubicBezierPoints

```python
CubicBezierPoints: TypeAlias = Union[
    npt.NDArray[PointDType], tuple[Point3D, Point3D, Point3D, Point3D]
]
"""``shape: (4, 3)``

A `Point3D_Array` of 4 control points for a single cubic Bézier
curve:
``[[float, float, float], [float, float, float], [float, float, float], [float, float, float]]``.
"""
```

### CubicBezierPoints_Array

```python
CubicBezierPoints_Array: TypeAlias = Union[
    npt.NDArray[PointDType], tuple[CubicBezierPoints, ...]
]
"""``shape: (N, 4, 3)``

An array of :math:`N` `CubicBezierPoints` objects:
``[[[float, float, float], [float, float, float], [float, float, float], [float, float, float]], ...]``.
"""
```

### CubicBezierPath

```python
CubicBezierPath: TypeAlias = Point3D_Array
"""``shape: (4*N, 3)``

A `Point3D_Array` of :math:`4N` points, where each one of the
:math:`N` consecutive blocks of 4 points represents a cubic Bézier
curve:
``[[float, float, float], ...], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### CubicSpline

```python
CubicSpline: TypeAlias = CubicBezierPath
"""``shape: (4*N, 3)``

A special case of `CubicBezierPath` where all the :math:`N` cubic
Bézier curves are connected, forming a quadratic spline:
``[[float, float, float], ...], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### BezierPoints

```python
BezierPoints: TypeAlias = Point3D_Array
r"""``shape: (PPC, 3)``

A `Point3D_Array` of :math:`\text{PPC}` control points
(:math:`\text{PPC: Points Per Curve} = n + 1`) for a single
:math:`n`-th degree Bézier curve:
``[[float, float, float], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### BezierPoints_Array

```python
BezierPoints_Array: TypeAlias = Union[npt.NDArray[PointDType], tuple[BezierPoints, ...]]
r"""``shape: (N, PPC, 3)``

An array of :math:`N` `BezierPoints` objects containing
:math:`\text{PPC}` `Point3D` objects each
(:math:`\text{PPC: Points Per Curve} = n + 1`):
``[[[float, float, float], ...], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### BezierPath

```python
BezierPath: TypeAlias = Point3D_Array
r"""``shape: (PPC*N, 3)``

A `Point3D_Array` of :math:`\text{PPC} \cdot N` points, where each
one of the :math:`N` consecutive blocks of :math:`\text{PPC}` control
points (:math:`\text{PPC: Points Per Curve} = n + 1`) represents a
Bézier curve of :math:`n`-th degree:
``[[float, float, float], ...], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### Spline

```python
Spline: TypeAlias = BezierPath
r"""``shape: (PPC*N, 3)``

A special case of `BezierPath` where all the :math:`N` Bézier curves
consisting of :math:`\text{PPC}` `Point3D` objects
(:math:`\text{PPC: Points Per Curve} = n + 1`) are connected, forming
an :math:`n`-th degree spline:
``[[float, float, float], ...], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### FlatBezierPoints

```python
FlatBezierPoints: TypeAlias = Union[npt.NDArray[PointDType], tuple[float, ...]]
"""``shape: (3*PPC*N,)``

A flattened array of Bézier control points:
``[float, ...]``.
"""
```
