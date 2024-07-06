## Vector Data Types

```python
"""
[CATEGORY]
Vector types
"""
```

### Vector2D

> [!caution]
> Do not confuse with the [[Vector#^manim-class-vector|Vector]] or [[Arrow#^manim-class-arrow|Arrow]]  [[VMObject#^manim-class-vmobject|VMobjects]]!

```python
Vector2D: TypeAlias = npt.NDArray[PointDType]
"""``shape: (2,)``

A 2-dimensional vector: ``[float, float]``.

Normally, a function or method which expects a `Vector2D` as a
parameter can handle being passed a `Vector3D` instead.

.. caution::
    Do not confuse with the :class:`~.Vector` or :class:`~.Arrow`
    VMobjects!
"""
```

### Vector2D_Array

```python
Vector2D_Array: TypeAlias = npt.NDArray[PointDType]
"""``shape: (M, 2)``

An array of `Vector2D` objects: ``[[float, float], ...]``.

Normally, a function or method which expects a `Vector2D_Array` as a
parameter can handle being passed a `Vector3D_Array` instead.
"""
```

### Vector3D

> [!caution]
> Do not confuse with the [[Vector#^manim-class-vector|Vector]] or [[Arrow3D#^manim-class-Arrow3D|Arrow3D]]  [[VMObject#^manim-class-vmobject|VMobjects]]!

```python
Vector3D: TypeAlias = npt.NDArray[PointDType]
"""``shape: (3,)``

A 3-dimensional vector: ``[float, float, float]``.

.. caution::
    Do not confuse with the :class:`~.Vector` or :class:`~.Arrow3D`
    VMobjects!
"""
```

### Vector3D_Array

```python
Vector3D_Array: TypeAlias = npt.NDArray[PointDType]
"""``shape: (M, 3)``

An array of `Vector3D` objects: ``[[float, float, float], ...]``.
"""
```

### VectorND

> [!caution]
> Do not confuse with the [[Vector#^manim-class-vector|Vector]] [[VMObject#^manim-class-vmobject|VMobject]]!
> 
> This type alias is named "VectorND" instead of "Vector" to avoid
> potential name collisions.

```python
VectorND: TypeAlias = npt.NDArray[PointDType]
"""``shape (N,)``

An :math:`N`-dimensional vector: ``[float, ...]``.

.. caution::
    Do not confuse with the :class:`~.Vector` VMobject! This type alias
    is named "VectorND" instead of "Vector" to avoid potential name
    collisions.
"""
```

### VectorND_Array

```python
VectorND_Array: TypeAlias = npt.NDArray[PointDType]
"""``shape (M, N)``

An array of `VectorND` objects: ``[[float, ...], ...]``.
"""
```

### RowVector

```python
RowVector: TypeAlias = npt.NDArray[PointDType]
"""``shape: (1, N)``

A row vector: ``[[float, ...]]``.
"""
```

### ColVector

```python
ColVector: TypeAlias = npt.NDArray[PointDType]
"""``shape: (N, 1)``

A column vector: ``[[float], [float], ...]``.
"""
```

