
%% #manim-typing %%

## Color Data Types

```python
"""
[CATEGORY]
Color types
"""
```

### ManimColorDType

```python
ManimColorDType: TypeAlias = ManimFloat
"""Data type used in :class:`~.ManimColorInternal`: a
double-precision float between 0 and 1.
"""
```

### RGB_Array_Float

```python
RGB_Array_Float: TypeAlias = npt.NDArray[ManimColorDType]
"""``shape: (3,)``

A :class:`numpy.ndarray` of 3 floats between 0 and 1, representing a
color in RGB format.

Its components describe, in order, the intensity of Red, Green, and
Blue in the represented color.
"""
```

### RGB_Tuple_Float

```python
RGB_Tuple_Float: TypeAlias = tuple[float, float, float]
"""``shape: (3,)``

A tuple of 3 floats between 0 and 1, representing a color in RGB
format.

Its components describe, in order, the intensity of Red, Green, and
Blue in the represented color.
"""
```

### RGB_Array_Int

```python
RGB_Array_Int: TypeAlias = npt.NDArray[ManimInt]
"""``shape: (3,)``

A :class:`numpy.ndarray` of 3 integers between 0 and 255,
representing a color in RGB format.

Its components describe, in order, the intensity of Red, Green, and
Blue in the represented color.
"""
```

### RGB_Tuple_Int

```python
RGB_Tuple_Int: TypeAlias = tuple[int, int, int]
"""``shape: (3,)``

A tuple of 3 integers between 0 and 255, representing a color in RGB
format.

Its components describe, in order, the intensity of Red, Green, and
Blue in the represented color.
"""
```

### RGBA_Array_Float

```python
RGBA_Array_Float: TypeAlias = npt.NDArray[ManimColorDType]
"""``shape: (4,)``

A :class:`numpy.ndarray` of 4 floats between 0 and 1, representing a
color in RGBA format.

Its components describe, in order, the intensity of Red, Green, Blue
and Alpha (opacity) in the represented color.
"""
```

### RGBA_Tuple_Float

```python
RGBA_Tuple_Float: TypeAlias = tuple[float, float, float, float]
"""``shape: (4,)``

A tuple of 4 floats between 0 and 1, representing a color in RGBA
format.

Its components describe, in order, the intensity of Red, Green, Blue
and Alpha (opacity) in the represented color.
"""
```

### RGBA_Array_Int

```python
RGBA_Array_Int: TypeAlias = npt.NDArray[ManimInt]
"""``shape: (4,)``

A :class:`numpy.ndarray` of 4 integers between 0 and 255,
representing a color in RGBA format.

Its components describe, in order, the intensity of Red, Green, Blue
and Alpha (opacity) in the represented color.
"""
```

### RGBA_Tuple_Int

```python
RGBA_Tuple_Int: TypeAlias = tuple[int, int, int, int]
"""``shape: (4,)``

A tuple of 4 integers between 0 and 255, representing a color in RGBA
format.

Its components describe, in order, the intensity of Red, Green, Blue
and Alpha (opacity) in the represented color.
"""
```

### HSV_Array_Float

```python
HSV_Array_Float: TypeAlias = RGB_Array_Float
"""``shape: (3,)``

A :class:`numpy.ndarray` of 3 floats between 0 and 1, representing a
color in HSV (or HSB) format.

Its components describe, in order, the Hue, Saturation and Value (or
Brightness) in the represented color.
"""
```

### HSV_Tuple_Float

```python
HSV_Tuple_Float: TypeAlias = RGB_Tuple_Float
"""``shape: (3,)``

A tuple of 3 floats between 0 and 1, representing a color in HSV (or
HSB) format.

Its components describe, in order, the Hue, Saturation and Value (or
Brightness) in the represented color.
"""
```

### ManimColorInternal

```python
ManimColorInternal: TypeAlias = RGBA_Array_Float
"""``shape: (4,)``

Internal color representation used by :class:`~.ManimColor`,
following the RGBA format.

It is a :class:`numpy.ndarray` consisting of 4 floats between 0 and
1, describing respectively the intensities of Red, Green, Blue and
Alpha (opacity) in the represented color.
"""
```



