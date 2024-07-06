## Image Data Types

```python
"""
[CATEGORY]
Image types
"""
```

### Image

```python
Image: TypeAlias = npt.NDArray[ManimInt]
"""``shape: (height, width) | (height, width, 3) | (height, width, 4)``

A rasterized image with a height of ``height`` pixels and a width of
``width`` pixels.

Every value in the array is an integer from 0 to 255.

Every pixel is represented either by a single integer indicating its
lightness (for greyscale images), an `RGB_Array_Int` or an
`RGBA_Array_Int`.
"""
```

### GrayscaleImage

```python
GrayscaleImage: TypeAlias = Image
"""``shape: (height, width)``

A 100% opaque grayscale `Image`, where every pixel value is a
`ManimInt` indicating its lightness (black -> gray -> white).
"""
```

### RGBImage

```python
RGBImage: TypeAlias = Image
"""``shape: (height, width, 3)``

A 100% opaque `Image` in color, where every pixel value is an
`RGB_Array_Int` object.
"""
```

### RGBAImage

```python
RGBAImage: TypeAlias = Image
"""``shape: (height, width, 4)``

An `Image` in color where pixels can be transparent. Every pixel
value is an `RGBA_Array_Int` object.
"""
```

