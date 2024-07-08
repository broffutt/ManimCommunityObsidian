
%% #py_source %%

# Py_CPYTHON_FLOATOBJECT_H

```c
#ifndef Py_CPYTHON_FLOATOBJECT_H
#  error "this header file must not be included directly"
#endif
```

Included via [[Manim Dependencies/python3.12.4/Include/floatobject.h|Py_FLOATOBJECT_H]]

## PyFloatObject

```c
typedef struct {
    PyObject_HEAD
    double ob_fval; // "object float value"
} PyFloatObject;
```

Type Refs:

