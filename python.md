# The Simtoonian Style Guide for Python
> [!WARNING]
> this style guide overrides the official PEP-8 style guide
---

## Specs

### Functions
Use snake_case for functions. For example, `def hello_world():`.

### Methods
Methods are functions that are class members. They are identified by the `self` parameter. Use snake_case for methods. For example, `def hello_world(self):`.

### Async functions/methods
Use snake_case for async functions/methods with the prefix `ASYNC_`. For example, `async def ASYNC_hello_world(self):`.

### Variables
Use camelCase for variables. For example, `myVar = "hello"`.

### Booleans
Use camelCase prefixed with `b` for booleans. For example, `bIsTrue = True`.

### Classes
Use PascalCase for classes. For example, `class MyModel:`.

### Constants
Use all caps for constants with an underscore between words. For example, `MY_CONSTANT = 1`.

### Modules
Use snake_case for modules. For example, `my_module.py`.

### String literals
Use double quotes for string literals. For example, `"This is a string"`.

### Typing
Use Python's `typing` module to annotate the types of variables, return types of functions/methods, etc. For example, `def my_method(myVariable: cv2.Mat) -> str:`. If the type is not a built-in type, use the fully qualified name of the type. For example, `def my_method(myVariable: cv2.Mat) -> str:`. All defined variables should be annotated with their types. For example, `myVar: int = 1`.

### Class attributes
To read and modify variables of classes, setters and getters should be used. For example, `obj.set_my_variable(1)` and `obj.get_my_variable()`.

### Conditionals
Place expressions into parentheses. Use `==` and `!=` for equality comparisons. For example, `if (myVar == 1):`. Conditionals should also use short-circuit evaluation, meaning that the most likely condition should be placed first, whether that is the positive or negative boolean condition.

### Logging
Use the `logging` module to log messages instead of print statements. For example, `logging.info("This is a message")`.
`logging.debug` shall be used for logging values that are likely to change often and would be important when debugging.
`logging.info` shall be used for printing resulting values (outputs), types of objects, etc.
`logging.warning` and `logging.error` shall be used when a possibly problematic value is encountered and when a breaking issue is encountered, respectively.

### Documentation
Use the Doxygen system to document your code. For example, `@param myVariable: This variable is an input to a function`.

### Comments
Use the `#` character to comment out code. For example, `# This is a comment`. For multi-line comments, use:
```python
"""
This is a
multi-line
comment
"""
```

### Imports
Use the `import` statement to import modules. For example, `import cv2`. Order your imports in the following order: standard library imports, third-party imports, local imports, where imports within each section are sorted alphabetically, and sections are separated by a blank line. For example:
```python
import os
import sys

import cv2
import numpy as np
import matplotlib.pyplot as plt

from my_module import my_method
```

### Other
Everything else should follow the official PEP-8 style guide.
