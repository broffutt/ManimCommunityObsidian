
## Path Data Types

```python
"""
[CATEGORY]
Path types
"""
```

### StrPath

```python
StrPath: TypeAlias = Union[str, PathLike[str]]
"""A string or :class:`os.PathLike` representing a path to a
directory or file.
"""
```

### StrOrBytesPath

```python
StrOrBytesPath: TypeAlias = Union[str, bytes, PathLike[str], PathLike[bytes]]
"""A string, bytes or :class:`os.PathLike` object representing a path
to a directory or file.
"""
```

