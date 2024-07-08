
%% #py_source  %%

# Py_FLOATOBJECT_H

```c
/* Float object interface */

/*
PyFloatObject represents a (double precision) floating point number.
*/

#ifndef Py_FLOATOBJECT_H
#define Py_FLOATOBJECT_H
```

## PyFloat_Type

```c
PyAPI_DATA(PyTypeObject) PyFloat_Type;
```

See [[pytypedefs.h#PyTypeObject|PyTypeObject]]

##

```c
#ifndef Py_LIMITED_API
#  define Py_CPYTHON_FLOATOBJECT_H
#  include "cpython/floatobject.h"
#  undef Py_CPYTHON_FLOATOBJECT_H
#endif

#endif /* !Py_FLOATOBJECT_H */
```

See [[Manim Dependencies/python3.12.4/Include/cpython/floatobject.h|Py_CPYTHON_FLOATOBJECT_H]]
