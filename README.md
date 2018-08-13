# TCPL Documentation
---
## 1. The Hello World Program

```
main {
    var console: Console, System.getRef.makeConsole;
    console.display;
    console.printLine("Hello, World!");
}

```
---
## 2. Constants and Variables

```
main {
    var console: Console, System.getRef.makeConsole;
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
## 3. Hardcoding

For any constant or variable you can specify its initial value after you
have specified its type:
```
var IDENTIFIER: TYPE, INITIAL_VALUE;
```
---
## 4. Primitive Data Types

| Keyword  | Description                                 |
|----------|:--------------------------------------------|
| `byte`   | 8 bit whole number                          |
| `short`  | 16 bit whole number                         |
| `int`    | 32 bit whole number                         |
| `long`   | 64 bit whole number                         |
| `float`  | 32 bit floating point number                |
| `double` | 64 bit floating point number                |
| `bool`   | 1 bit value, may contain only true or false |
| `char`   | character                                   |

**Note:** Whole numbers may have the `unsigned` modifier attached to them.
This determines wheteher the numbers may hold negative values. Whole
numbers are signed by default, and floating point numbers are always
unsigned. The `char` data type is neither signed nor unsigned, because
it's not treated as a number by the standard.

## 5. Composite Data Types

TCPL provides object-oriented facilities, which makes it possible to define
a whole slew of data types containing the primitive types. The way to do
this is via classes:

```
class ExampleClass {
private:
    var a: int;
    var b: float;
public:
    def __init__(a: int, b: float) {
        self.a = a;
        self.b = b;
    }
    def __fin__ {
        var console: Console, System.getRef.makeConsole;
        console.display;
        console.printLine(
                "Object of type ExampleClass has been destroyed.");
    }
}
```
