
%% #manim-typing %%

## Point Data Types

```python
"""
[CATEGORY]
Point types
"""
```

### PointDType

```python
PointDType: TypeAlias = ManimFloat
"""Default type for arrays representing points: a double-precision
floating point value.
"""
```

### InternalPoint2D

> [!note]
> This type alias is mostly made available for internal use, and
> only includes the NumPy type.

```python
InternalPoint2D: TypeAlias = npt.NDArray[PointDType]
"""``shape: (2,)``

A 2-dimensional point: ``[float, float]``.

.. note::
    This type alias is mostly made available for internal use, and
    only includes the NumPy type.
"""
```

### Point2D

```python
Point2D: TypeAlias = Union[InternalPoint2D, tuple[float, float]]
"""``shape: (2,)``

A 2-dimensional point: ``[float, float]``.

Normally, a function or method which expects a `Point2D` as a
parameter can handle being passed a `Point3D` instead.
"""
```

### InternalPoint2D_Array

> [!note]
> This type alias is mostly made available for internal use, and
> only includes the NumPy type.

```python
InternalPoint2D_Array: TypeAlias = npt.NDArray[PointDType]
"""``shape: (N, 2)``

An array of `InternalPoint2D` objects: ``[[float, float], ...]``.

.. note::
    This type alias is mostly made available for internal use, and
    only includes the NumPy type.
"""
```

### Point2D_Array

```python
Point2D_Array: TypeAlias = Union[InternalPoint2D_Array, tuple[Point2D, ...]]
"""``shape: (N, 2)``

An array of `Point2D` objects: ``[[float, float], ...]``.

Normally, a function or method which expects a `Point2D_Array` as a
parameter can handle being passed a `Point3D_Array` instead.

Please refer to the documentation of the function you are using for
further type information.
"""
```

### InternalPoint3D

> [!note]
> This type alias is mostly made available for internal use, and
> only includes the NumPy type.

```python
InternalPoint3D: TypeAlias = npt.NDArray[PointDType]
"""``shape: (3,)``

A 3-dimensional point: ``[float, float, float]``.

.. note::
    This type alias is mostly made available for internal use, and
    only includes the NumPy type.
"""
```

### Point3D

```python
Point3D: TypeAlias = Union[InternalPoint3D, tuple[float, float, float]]
"""``shape: (3,)``

A 3-dimensional point: ``[float, float, float]``.
"""
```

### InternalPoint3D_Array

> [!note]
> This type alias is mostly made available for internal use, and
> only includes the NumPy type.

```python
InternalPoint3D_Array: TypeAlias = npt.NDArray[PointDType]
"""``shape: (N, 3)``

An array of `Point3D` objects: ``[[float, float, float], ...]``.

.. note::
    This type alias is mostly made available for internal use, and
    only includes the NumPy type.
"""
```

### Point3D_Array

```python
Point3D_Array: TypeAlias = Union[InternalPoint3D_Array, tuple[Point3D, ...]]
"""``shape: (N, 3)``

An array of `Point3D` objects: ``[[float, float, float], ...]``.

Please refer to the documentation of the function you are using for
further type information.
"""
```

