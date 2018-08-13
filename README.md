# TCPL Documentation
---
## 1. The Hello World Program

```
from system.io using System, Console

main {
    Console console = System.getRef.makeConsole;
    console.display;
    console.printLine("Hello, World!");
}

```
---
## 2. Constants and Variables

```
from system.io using System, Console

main {
    Console console = System.getRef.makeConsole;
    console.display;
    var a: int, 1;
    val b: int, 2;
    console.printLine("a is a variable. Its value is ", a);
    console.printLine("b is a constant. Its values is", b,
            "It cannot be changed.");
    a = 3;
    console.printLine("Now the value of a is", a);
}
```
---
## 3. Primitive Data Types

| Keyword  | Description                                 |
|----------|---------------------------------------------|
| `byte`   | 8 bit whole number                          |
| `short`  | 16 bit whole number                         |
| `int`    | 32 bit whole number                         |
| `long`   | 64 bit whole number                         |
| `float`  | 32 bit floating point number                |
| `double` | 64 bit floating point number                |
| `bool`   | 1 bit value, may contain only true or false |
| `char`   | character                                   |

*Note: Whole numbers may have the **unsigned** modifier attached to them.
This determines wheteher the numbers may hold negative values. Whole
numbers are signed by default, and floating point numbers are always
unsigned. The **char** data type is neither signed nor unsigned, because
it's not treated as a number by the standard.*

## 4. Composite Data Types

