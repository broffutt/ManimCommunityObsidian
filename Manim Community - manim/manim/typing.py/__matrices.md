
%% #manim-typing %%

## Matrix Data Types

```python
"""
[CATEGORY]
Matrix types
"""
```

### MatrixMN

```python
MatrixMN: TypeAlias = npt.NDArray[PointDType]
"""``shape: (M, N)``

A matrix: ``[[float, ...], [float, ...], ...]``.
"""
```

### Zeros

```python
Zeros: TypeAlias = MatrixMN
"""``shape: (M, N)``

A `MatrixMN` filled with zeros, typically created with
``numpy.zeros((M, N))``.
"""
```

