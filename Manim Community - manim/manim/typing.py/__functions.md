
%% #manim-typing %%

## Function Data Types

```python
"""
[CATEGORY]
Function types
"""
```

### FunctionOverride

```python
# Due to current limitations
# (see https://github.com/python/mypy/issues/14656 / 8263),
# we don't specify the first argument type (Mobject).
# Nor are we able to specify the return type (Animation) since we cannot import
# that here.
FunctionOverride: TypeAlias = Callable
"""Function type returning an :class:`~.Animation` for the specified
:class:`~.Mobject`.
"""
```

### PathFuncType

```python
PathFuncType: TypeAlias = Callable[[Point3D, Point3D, float], Point3D]
"""Function mapping two `Point3D` objects and an alpha value to a new
`Point3D`.
"""
```

### MappingFunction

```python
MappingFunction: TypeAlias = Callable[[Point3D], Point3D]
"""A function mapping a `Point3D` to another `Point3D`."""
```
