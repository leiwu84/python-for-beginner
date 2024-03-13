## Basic Types

### Built-in Data Types

- Type: `NoneType`. Only one value: `None`.
- Type: `bool`. Only two values: `True` and `False`. 
- Type: `int`. Examples: `-1`, `0`, `1`, `2`, `3`, ...
- Type: `float`. Examples: `-1.1`, `0.5`, `1.0`, `23.456`, ...
- Type: `complex`. Examples: `1 + 2j`, `-1.5 + 123.45j`, ...
- Type: `str`. Examples: `'Hello World'`, `"name"`, `'Monday'`, ...
- ...


### String

Enclosed by a pair of quotation marks.

`'This is a string'`

`"This is a string, too"`

```py
"""
This is a string over multiple lines.
Line 1.
Line 2.
"""
```

### Tuple

- The built-in type is `tuple`. Enclosed by `(` `)`. Elements are separated by comma `,`.
- Examples:
    - `(1, 2, 3)`
    - `('a', 'b')`
    - `(True, 100, -1.5, 1+2j, 'name', None, [1, 2])`
    - Nested tuple: `(('apple', 'orange'), (1, 2, 3), 4, 5)`

#### Access Elements
Use the index enclosed by `[` `]`. The index starts from `0`.
```py
fruits_tuple = ('apple', 'orange', ('banana', 'berry'))

print(fruits_tuple[0])
print(fruits_tuple[2][0])
```

### List

- The built-in type is `list`. Enclosed by `[` `]`. Elements are separated by comma `,`.
- Examples: 
    - `[1, 2, 3]`
    - `['a', 'b']`
    - `[True, 100, -1.5, 1+2j, 'name', None, (1, 2)]`
    - Nested list: `[['apple', 'orange'], [1, 2, 3], 4, 5]`

#### Access Elements
Use the index enclosed by `[` `]`. The index starts from `0`.
```py
fruits_list = ['apple', 'orange', ['banana', 'berry']]

print(fruits_list[1])
print(fruits_list[2][1])
```

### Dict

- The built-in type is `dict`. Enclosed by `{` `}`. Elements are pairs of key-values. Each pair is defined in the format of `key: value`. Pairs are separated by comma `,`.
- Examples:
    - `{'name': 'apple', 'color': 'red', 'price': 1.23}`
    - `{1:  'first', 2: '2nd', 3: 'third', 4: None}`
    - Nested dictionary: 
    `{'name': 'apple', 'prop': {'color': 'red', 'price': 1.23}}`

#### Access Elements
Use the key enclosed by `[` `]`. The key is defined in each kay-value pair. 
```py
fruits = {'name': 'apple', 'prop': {'color': 'red', 'price': 1.23}}

print(fruits['name'])
print(fruits['prop']['color'])
```

## Operators

- `+`, `-`, `*`, `/`, `**`, `%`
    - With numbers, e.g. : `1 + 1`, `3 - 1.5`, `2*3`, `4**0.5`, `30/7`, `30%7`
    - With strings, e.g.: `'Today' + ' ' + 'is ' + 'Tuesday.'`
    - With lists, e.g.: `[1]*3`, `['apple']*3`, `[None]*3`
- `>`, `<`, `==`, `>=`, `<=`
    * `5 > 3`, `-1 == 10`, `5 <= 3`, `'A' < 'B'`

---
## Assignment

Assign any type of data a name by the symbol `=`.

Examples:

```py
a = 1
fruit = 'apple'
integers = [1, 2, 3]
credentials = {'user': 'Me', 'pass': '***'}
```

```py
total = 1 + 1
msg = 'Today is' + ' Tuesday.'
is_less = 3 < 4
```

### Benefit of Assignment
Reuse in other expressions.
```py
a = 2
b = a * 3
c, d = 'Hello ', 'World.'
greeting = c + d 
```

---
## Naming style
- Alphanumeric (`A`-`Z`, `0`-`9`) and underscore `_`
- Recommendation: 
    - Short but informative.
    - For constants, all in upper case
        - E.g. `COLOR = '#00FF00'`, `MY_AGE = 18`.
    - For variables, all in lower case
        - E.g. `class_room_2` instead of `cr2` or `x`.

---
## Comments

Anything after the symble `#` is treated as comments.

```py
a = 1 * 2  # Explain the code
# If you need to write more,
# You can use multiple lines.
```

---
## Block and Indentation
Its design philosophy emphasizes code readability with the use of significant indentation. 

Syntax
```py
expression:
    line_1
    line_2
```

- The first line is not indented, ended by a colon `:`
- The following lines in the block must be indented with the same number of spaces. A common practice is four spaces.

---
## Loops
Loops let the program iteratively run a block of code.

- `while`-loop
- `for`-loop

---
## While Loop
```py
while expression:
    block of statements
```
If the expression is `True`, then executes the block of statements.
Otherwise, the `while`-loop is finished. Example:
```py
count = 1
while count < 5:
    print(count)
    count += 1
```

---
## For Loop
```py
for elem in a_sequence:
    block of statements
```
If all the elements in the sequence is used, the `for`-loop is finished. Example:
```py
for count in [1, 2, 3, 4]:
    print(count)
```
---
## Function


### Syntax of definition
```py hl_lines="1"
def func_name(param_1, param_2, param_3=3):
    """
    Docstring explains the purpose, 
    inputs, and returns of this function.
    """
    return param_1 + param_2 - param_3
```

Note the definition of the function can have 2 different kinds of input parameters.

- _Positional parameter_ - A positional parameter does not have a defaul value, like `param_1` and `param_2` in this example.
- _Keyword parameter_ - A keyword parameter has a defaul value, like `param_3` in this example.

!!! info
    When defining a function, positional parameters must be defined before keyword parameters. And accordingly, when calling a function, the positional argument 

### Example of call
```py hl_lines="7"
# Use the function name followed by all the
#   arguments, enclosed by ().
# 1 is a positional argument for the positional parameter param_1
# param_2=2 is a keyword argument for the positional parameter param_2
# param_3=4 is a keyword argument for the keyword parameter param_2
# The returned is assigned to variable res.
res = func_name(1, param_2=2, param_3=4)
print(res)
```

!!! info "Terminology"
    - **Input parameter**: An input that is in the _definition_ of a function.
    - **Argument**: An input that is provided when _calling_ a function.

!!! info
    It is allowed to provide keyword argument to a positional parameter, like `param_2` in this example. And it is commonly a good practice to always use keyword argument for every input parameter, no matter if it is defined as a positional or keyword parameter, since it is more readable and it doesn't require the order of the arguments to be same as the definition. 
    
    Here because `param_2` is provided as a keyword argument, it can be written after `param_3`. But `param_1` is provided as a positional argument, it has to be the first argument. 

    ```py
    res = func_name(1, param_3=4, param_2=2)  # Allowed.
    ```

---
## Class

### Syntax of definition
```py
class ClassName:
    def __init__(self, param_1, param_2):
        self.param_1 = param_1  # attribute
        self.param_2 = param_2  # attribute

    def run(self, param_3):  # method
        res = self.param_1 + self.param_2 - param_3
        return res
```

### Example of instance
```py
# Create an instance of the class
# Provide arguments to the __init__ method.
instance_1 = ClassName(1, param_2=2)

# Call a method
#  use the dot sign "." followed by the method name
res = instance_1.run(param_3=3)
print(res)
```

---
## Import
Import an object from other files in the same folder and other folder to the current file.

```py
import module_1
import module_2 as new_name
from module_3 import ClassName, func_name, CONSTANT_1
from package_4 import module_4
from pacakge_5.module_5 import func_name_5
```

---
## Examples of Import

```py
import sys
import multiprocessing as mp
from datetime import date

print(sys.platform)
print(mp.cpu_count())
print(date.today())
```