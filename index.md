---
layout: page
title: Learning Python
toc: true
---

- [1. Introduction](#1-introduction)
- [2. Setting up the environment](#2-setting-up-the-environment)
  - [2.1. Using devcontainers](#21-using-devcontainers)
  - [2.2. Using WSL2](#22-using-wsl2)
- [3. Your first Python application](#3-your-first-python-application)
- [4. Python syntax](#4-python-syntax)
  - [4.1. Indentation](#41-indentation)
  - [4.2. Comments](#42-comments)
- [5. Variables](#5-variables)
  - [5.1. The basics about variables](#51-the-basics-about-variables)
  - [5.2. Different data types](#52-different-data-types)
  - [5.3. Casting variables](#53-casting-variables)
  - [5.4. Getting a variable type](#54-getting-a-variable-type)
  - [5.5. Variable scope](#55-variable-scope)
- [6. Strings](#6-strings)
  - [6.1. The basics about strings](#61-the-basics-about-strings)
  - [6.2. Strings are arrays](#62-strings-are-arrays)
  - [6.3. String length](#63-string-length)
  - [6.4. Checking a string](#64-checking-a-string)
  - [6.5. Slicing strings](#65-slicing-strings)
  - [6.6. Convert your string to upper or lower case](#66-convert-your-string-to-upper-or-lower-case)
  - [6.7. Trim a string](#67-trim-a-string)
  - [6.8. Replacing a string](#68-replacing-a-string)
  - [6.9. Split a string](#69-split-a-string)
  - [6.10. Formatting strings](#610-formatting-strings)
  - [6.11. Escape characters](#611-escape-characters)
- [7. Numbers](#7-numbers)
  - [7.1. The basics about numbers](#71-the-basics-about-numbers)
  - [7.2. Type conversion](#72-type-conversion)
  - [7.3. Generate a random number](#73-generate-a-random-number)
  - [7.4. Absolute value](#74-absolute-value)
  - [7.5. Using the math module](#75-using-the-math-module)
  - [7.6. Converting between decimal, binary, octal, and hexadecimal](#76-converting-between-decimal-binary-octal-and-hexadecimal)
- [8. Booleans](#8-booleans)
  - [8.1. The basics about booleans](#81-the-basics-about-booleans)
  - [8.2. Some values are false](#82-some-values-are-false)
  - [8.3. Functions can also return a boolean](#83-functions-can-also-return-a-boolean)
- [9. Operators](#9-operators)
  - [9.1. Arithmetic operators](#91-arithmetic-operators)
  - [9.2. Comparison operators](#92-comparison-operators)
  - [9.3. Logical operators](#93-logical-operators)
  - [9.4. Identity operators](#94-identity-operators)
  - [9.5. Membership operators](#95-membership-operators)
  - [9.6. Bitwise operators](#96-bitwise-operators)
  - [9.7. Assignment operators](#97-assignment-operators)
- [10. Python Collections](#10-python-collections)
  - [10.1. Lists](#101-lists)
  - [10.2. Tuples](#102-tuples)
  - [10.3. Sets](#103-sets)
  - [10.4. Dictionaries](#104-dictionaries)
  - [10.5. Arrays](#105-arrays)
- [11. Conditions](#11-conditions)
  - [11.1. if-then-elif](#111-if-then-elif)
  - [11.2. if-then-else](#112-if-then-else)
  - [11.3. Nested if-then-else](#113-nested-if-then-else)
  - [11.4. Logical operators](#114-logical-operators)
  - [11.5. Shorthand and Conditional Expressions](#115-shorthand-and-conditional-expressions)
- [12. Using Functions](#12-using-functions)
  - [12.1. The basics about functions](#121-the-basics-about-functions)
  - [12.2. Introduction to Lambda](#122-introduction-to-lambda)
  - [12.3. Using Lambda functions](#123-using-lambda-functions)
- [13. Loops](#13-loops)
  - [13.1. While loop](#131-while-loop)
  - [13.2. For loop](#132-for-loop)
- [14. User Input](#14-user-input)
- [15. Exception handling](#15-exception-handling)
  - [15.1. The basics about exceptions](#151-the-basics-about-exceptions)
  - [15.2. Raise an exception](#152-raise-an-exception)
- [16. Working with Files](#16-working-with-files)
  - [16.1. Syntax](#161-syntax)
  - [16.2. Reading files](#162-reading-files)
  - [16.3. Closing](#163-closing)
  - [16.4. Writing files](#164-writing-files)
  - [16.5. Create a new file](#165-create-a-new-file)
  - [16.6. Delete a file or folder](#166-delete-a-file-or-folder)
- [17. Modules](#17-modules)
  - [17.1. Using a module](#171-using-a-module)
  - [17.2. Using variable in modules](#172-using-variable-in-modules)
  - [17.3. Import from a module](#173-import-from-a-module)
  - [17.4. Rename a module](#174-rename-a-module)
  - [17.5. Built-in modules](#175-built-in-modules)
- [18. Classes](#18-classes)
  - [18.1. Creating a class and object](#181-creating-a-class-and-object)
  - [18.2. The constructor method](#182-the-constructor-method)
  - [18.3. Define an object method](#183-define-an-object-method)
  - [18.4. The self parameter](#184-the-self-parameter)
  - [18.5. Object actions](#185-object-actions)
  - [18.6. Inheritance](#186-inheritance)
- [19. Iterators](#19-iterators)
  - [19.1. The basics about iterators](#191-the-basics-about-iterators)
  - [19.2. Creating an iterator](#192-creating-an-iterator)
- [20. PIP: Using packages and virtual environments](#20-pip-using-packages-and-virtual-environments)
  - [20.1. Create and start the virtual environment](#201-create-and-start-the-virtual-environment)
  - [20.2. Managing packages with pip](#202-managing-packages-with-pip)
  - [20.3. Install all dependencies](#203-install-all-dependencies)

## 1. Introduction

[Python][Python] is a language specification with multiple implementations like CPython, Jython, and MicroPython, but almost everyone refers to the CPython implementation as Python that can be found on almost every Linux server. The MicroPython implementation is to run Python on microcontrollers. Jython is the last big implementation of Python 2 that runs on the Java Virtual Machine and development has mostly stalled, but development for Python 3.8 support has recently started.

The Python Institute also has a certification traject with three levels called [PCEP], [PCAP], and [PCPP]. As the PCAP exam also covers the PCEP objectives most people directly take this exam. The PCPP covers the Python ecosystem part and more advantage architecture patterns.

## 2. Setting up the environment

### 2.1. Using devcontainers

Learning Python can be done on any system with a text-editor and the Python interpreter. But it is advised to an editor like [Visual Studio Code][vscode] to help you develop your code. Also, VSCode can help you by spinning up a [Python development container][python-devcontainer] in Docker to make sure everything installed and configured correctly everytime.

- Install Git on [Windows][git-win]
- [Setup VSCode](https://code.visualstudio.com/docs/setup/setup-overview)
- [Developing inside a Container][vscode-containers]

When you have everything working correctly then [python-template][python-template] repository should start a Python based development container. In the terminal window within VSCode we can start Python manually as below

```shell
vscode@03fdf48d4d7f python-template (master) $ python
Python 3.9.1 (default, Jan 12 2021, 16:56:42) 
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

### 2.2. Using WSL2

- Install Git on [Windows][git-win]
- [Setup VSCode](https://code.visualstudio.com/docs/setup/setup-overview)
- [Developing in WSL][vscode-wsl]

<!--nextpage-->
## 3. Your first Python application

Let start directly with the famous `Hello World` application in the Python shell. The Python shell can be used for very short applications like to run `print("Hello World")`.

```shell
$ python
Python 3.9.1 (default, Jan 12 2021, 16:56:42) 
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello World.")
Hello World.
>>>
```

Python can also use file as the source to run the `Hello World` application and if we create a file `hello.py` with the content below we can execute it later.

```python
print("Hello World.")
```

Python can now use the file `hello.py` as a source and it nicely prints `Hello World.` to the screen.

```shell
$ python hello.py
Hello World.
```

Now that we have a quick and dirty way of running `Hello World.` we can take it to the next level and turn it a proper Python program you can execute on every Unix-like system with Python 3 installed. If we replace the content of `hello.py` with the example below then we can run it it again and should still give `Hello World.`

```python
#!/usr/bin/env python3

def main():
    print("Hello World.")


if __name__ == "__main__":
    main()
```

If we also add the execute bit to the file `hello.py` we can directly start it without prefexing it the Python interpreter. And again we get `Hello World.` on the screen.

```shell
$ chmod +x hello.py
$ hello.py
Hello World
```

But what does this all mean? Let start with the first line where tell unix via a [shebang][shebang] to look the `python3` interpreter via the `env` command. This guarantees that we always find the Python interpreter while we don't set any hardcoded paths. In the [PIP](pip) section we will go deeping into why this important when we start working with virtual environments.

```python
#!/usr/bin/env python3
```

Secondly we define a function called `main` and we put the print statement for `Hello World.` in this function. One thing that is different from other languages is that indentation is important and gives context to the statement.

```python
def main():
    print("Hello World.")
```

The third section is that we call the function called `main` if we execute the file `hello.py`. The exact reason for why we do this is explained in the [modules](modules) section.

```python
if __name__ == "__main__":
    main()
```

> Most examples will be based on this example and the `main` function will be modified.

<!--nextpage-->
## 4. Python syntax

### 4.1. Indentation

Python depends on indentation to follow the correct flow of execution. In the example below we see that there is a possible error as `Hello Jack.` is being printed before anything else. Many will assume it will be printed after `Hello John.` as it is directly after it, but indentation wise it isn't part of the `main` function.

```python
#!/usr/bin/env python3

def main():
    if 1 > 2:
        print("Hello World.")
    print("Hello John.")
print("Hello Jack.")


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello Jack.
Hello John.
```

If we try to correct this error by adding a space before the print statement, then Python still gives an error as indentation doesn't match all other levels. Python is very similar like YAML and all the indentation need to be the same. See [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/#indentation) for a complete set of rules about indentation.

```python
#!/usr/bin/env python3

def main():
    if 1 > 2:
        print("Hello World.")
    print("Hello John.")
 print("Hello Jack.")


if __name__ == "__main__":
    main()
```

Output:

```shell
  File "/workspaces/python-examples/hello.py", line 7
    print("Hello Jack.")
                        ^
IndentationError: unindent does not match any outer indentation level
```

### 4.2. Comments

Any line that starts with `#` will be ignored by Python.

```python
#!/usr/bin/env python3

def main():
    if 1 > 2:
        print("Hello World.")
    print("Hello John.")
    # print("Hello Jack.")


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello John.
```

Multiline comments can be done by starting every line with the `#`-sign.

```python
#!/usr/bin/env python3

def main():
    if 1 > 2:
        print("Hello World.")
    print("Hello John.")
    # print("Hello Jack.")
    # print("Hello James.")


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello John.
```

For multiline comments Python also supports comments between triple quotes as in the example below.

```python
#!/usr/bin/env python3

def main():
    if 1 > 2:
        print("Hello World.")
    print("Hello John.")
    """
    print("Hello Jack.")
    print("Hello James.")
    """


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello John.
```

<!--nextpage-->
## 5. Variables

No programs works without variables to store data values in while the program runs. Variables in Python are strong dynamically typed which mean you can change a variable from a number to a string by assignment, but a variable will not become a number when a string contains a number for example. This also means you may have to cast variable from a number to a string in some cases or vice versa.

### 5.1. The basics about variables

Let start with basic example based on our `Hello World.` application where we have two lines. And in this example we still present print directly with a string telling about two people called John and their age.

```python
def main():
    print("My name is John and I am 42.")
    print("My name is John and I am also 42.")
```

Output:

```shell
My name is John and I am 42.
My name is John and I am also 42
```

Lets put the name and age both in their own variable as a string and update the strings to concatenate the whole string together. Here we that Python used the `+`-sign to concatenate strings together.

```python
def main():
    name = "John"
    age = "42"
    print("My name is " + name + " and I am " + age + ".")
    print("My name is " + name + " and I am also " + age + ".")
```

Output:

```shell
My name is John and I am 42.
My name is John and I am also 42
```

```python
def main():
    name = "John"
    age = "42"
    print("My name is " + name + " and I am " + age + ".")
    name = "Jack"
    print("My name is " + name + " and I am also " + age + ".")
```

Output:

```shell
My name is John and I am 42.
My name is Jack and I am also 42
```

### 5.2. Different data types

Python has the following data types built-in by default, in these categories:

| Category        | Data type                    |
| :-------------- | :--------------------------- |
| Text Type:      | str                          |
| Numeric Types:  | int, float, complex          |
| Sequence Types: | list, tuple, range           |
| Mapping Type:   | dict                         |
| Set Types:      | set, frozenset               |
| Boolean Type:   | bool                         |
| Binary Types:   | bytes, bytearray, memoryview |

### 5.3. Casting variables

Python is flexible with its data types for variables, but Python does require type casting in some cases. Using a variable that contains a number that needs to concatenated with a string needs to be casted from an integer to a string. In the example below we forget to type cast a string and it fails.

```python
def main():
    name = "John"
    age = 42
    print("My name is " + name + " and I am " + age + ".")
```

Output:

```shell
Traceback (most recent call last):
  File "/workspaces/python-examples/v03.py", line 10, in <module>
    main()
  File "/workspaces/python-examples/v03.py", line 6, in main
    print("My name is " + name + " and I am " + age + ".")
TypeError: can only concatenate str (not "int") to str
```

If we type cast the variable `age` from integer to string with the `str()` function it works perfectly. Other functions to type cast are `int()` and `float()`.

```python
def main():
    name = "John"
    age = 42
    print("My name is " + name + " and I am " + str(age) + ".")
```

### 5.4. Getting a variable type

Python can also determine the data type of a variable with `type()`. This can become useful when importing data from unknown source and needs validation.

```python
def main():
    name = "John"
    age = 42
    print(type(name))
    print(type(age))
```

Output:

```shell
<class 'str'>
<class 'int'>
```

### 5.5. Variable scope

Variables are scope sensitive and in the example below we define the variable on a global level and can be read scopes of functions and methods. Having global variables isn't a good idea as it leads to messy programming. For constants this is fine, but the variables should only be read from and not updated.

```python
#!/usr/bin/env python3

phrase = "Hello World."

def main():
    print(phrase)


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello World.
```

Variables can have a global and local scope. In the example below we set the variable on a global level, but override it with a different value as a local variable/

```python
#!/usr/bin/env python3

phrase = "Hello World."

def main():
    phrase = "Hello People."
    print(phrase)


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello People.
```

Python also has the option to turn local variables in global variables as in the example below. The extra function `setup()` uses the keyword `global` to make the variable `x` a global variable.

```python
#!/usr/bin/env python3

phrase = "Hello World."

def setup():
    global phrase
    phrase = "Hello People."


def main():
    print(phrase)


if __name__ == "__main__":
    setup()
    main()
```

Output:

```shell
Hello People.
```

> Using global variables is considert bad programming and a risk as it can have unforeseen effects.

<!--nextpage-->
## 6. Strings

In Python strings are surrounds by either single quotation marks, or double quotation marks. [PEP 8][pep-0008] describes no standard on how to use single or double-quotes:

> In Python, single-quoted strings and double-quoted strings are the same. This PEP does not make a recommendation for this. Pick a rule and stick to it. When a string contains single or double quote characters, however, use the other one to avoid backslashes in the string. It improves readability.
>
> For triple-quoted strings, always use double quote characters to be consistent with the docstring convention in [PEP 257][pep-0257].

Some tools like [Black][black] have a preference to have all strings and comments in double quotes, but both ways are correct.

### 6.1. The basics about strings

The most basic form of a string is one that is given directly to `print()`.

```python
#!/usr/bin/env python3

def main():
    print("Hello World.")


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello World.
```

The second form is to assign a variable to a string and can be used by `print()` as a reference to the string.

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase)


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello World.
```

As seen in the [Variables](#5-variables) section, variables can be joined with the `+`-sign and a string can also be concatenated with a variable.

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    phrase_two = "And Goodbye."
    # Concatenate two variables
    print(phrase_one + phrase_two)
    # Concatenate two variables with a string
    print(phrase_one + " " + phrase_two)


if __name__ == "__main__":
    main()
```

Output:

```shel
Hello World.And Goodbye.
Hello World. And Goodbye.
```

Strings can also be a multiline string with a newline character as part of the value. Python does take the indentation of a multiline string not into account and will the indentation will be part of the string. On Stack Overflow in [question 2504411][stackoverflow-2504411] possible solutions to work around this issue are discusses.

```python
#!/usr/bin/env python3

def main():
    phrase_one = """Hello World.
    And Goodbye."""
    print(phrase_one)


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello World.
    And Goodbye.
```

### 6.2. Strings are arrays

Strings are like in other languages arrays and can be address in that way. The working of arrays is described in [Arrays](#85-arrays), but for now we read the second element of the array and print it.

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one[1])


if __name__ == "__main__":
    main()
```

Output:

```shell
e
```

As a strings is an array you can easily [loop](#122-for-loop) over all elements and get every element separately.

```python
#!/usr/bin/env python3

def main():
    for x in "Hello World.":
        print(x)


if __name__ == "__main__":
    main()
```

Output:

```shell
H
e
l
l
o
 
W
o
r
l
d
.
```

### 6.3. String length

The built-in function `len()` return the length of an object and used the internal method `__len__()` of the object to determine the length.

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    # Using the built-in version
    print(len(phrase_one))
    # Using the internal method of an object
    print(phrase_one.__len__())


if __name__ == "__main__":
    main()
```

```shell
12
12
```

### 6.4. Checking a string

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print("Hello" in phrase_one)


if __name__ == "__main__":
    main()
```

Output:

```shell
True
```

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    if "Hello" in phrase_one:
        print("Yes, Hello World.")


if __name__ == "__main__":
    main()
```

Output:

```shell
Yes, Hello World.
```

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    if "Hello" not in phrase_one:
        print("Yes, Hello World.")
    else:
        print("No, Hello World.")


if __name__ == "__main__":
    main()
```

Output:

```shell
No, Hello World.
```

### 6.5. Slicing strings

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one[2:5])


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one[:5])


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one[2:])


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one[-5:-2])


if __name__ == "__main__":
    main()
```

### 6.6. Convert your string to upper or lower case

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one.upper())


if __name__ == "__main__":
    main()
```

Output:

```shell
HELLO WORLD.
```

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one.lower())


if __name__ == "__main__":
    main()
```

Output:

```shell
hello world.
```

### 6.7. Trim a string

The method `strip()` removes by default whitespace character from the string on both sides. With `lstrip()` or `rstrip()` the string is only being trimmed on the left or ride side.

```python
#!/usr/bin/env python3

def main():
    phrase_one = " Hello World. "
    print(phrase_one)
    print(phrase_one.strip())


if __name__ == "__main__":
    main()
```

Output:

```shell
 Hello World.
Hello World.
```

The method `strip` by default trims whitespace characters, but can also use other characters to trim a string.

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one.strip("HeldW."))


if __name__ == "__main__":
    main()
```

Output:

```shell
o Wor
```

### 6.8. Replacing a string

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one.replace("W", "w"))


if __name__ == "__main__":
    main()
```

### 6.9. Split a string

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello World."
    print(phrase_one.split(" "))


if __name__ == "__main__":
    main()
```

`join`

### 6.10. Formatting strings

```python
#!/usr/bin/env python3

def main():
    name_one = "World"
    phrase_one = "Hello {}."
    print(phrase_one.format(name_one))


if __name__ == "__main__":
    main()
```

Output:

```shell
Hello World.
```

```python
#!/usr/bin/env python3

def main():
    name_one = "Jack"
    name_two = "John"
    phrase_one = "Hello {} and {}."
    print(phrase_one.format(name_one, name_two))


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    name_one = "Jack"
    name_two = "John"
    phrase_one = "Hello {1} and {0}."
    print(phrase_one.format(name_one, name_two))


if __name__ == "__main__":
    main()
```

### 6.11. Escape characters

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello "World"."
    print(phrase_one)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    phrase_one = "Hello \"World\"."
    print(phrase_one)


if __name__ == "__main__":
    main()
```

| Code  | Result          |
| :---: | :-------------- |
|  \\'  | Single Quote    |
| \\\\  | Backslash       |
|  \n   | New Line        |
|  \r   | Carriage Return |
|  \t   | Tab             |
|  \b   | Backspace       |
|  \f   | Form Feed       |
| \ooo  | Octal value     |
| \xhh  | Hex value       |

<!--nextpage-->
## 7. Numbers

- `int`
- `float`
- `complex`

### 7.1. The basics about numbers

```python
#!/usr/bin/env python3

def main():
    q = -1
    x = 1
    y = 3.14
    z = 1j
    print(type(q))
    print(type(x))
    print(type(y))
    print(type(z))


if __name__ == "__main__":
    main()
```

```shell
<class 'int'>
<class 'int'>
<class 'float'>
<class 'complex'>
```

### 7.2. Type conversion

Complex numbers cannot be converted into another number type

```python
#!/usr/bin/env python3

def main():
    x = 1
    y = 3.14
    z = 1j

    a = float(x)
    b = float(y)

    print(a)
    print(b)

    print(type(a))
    print(type(b))


if __name__ == "__main__":
    main()
```

### 7.3. Generate a random number

```python
#!/usr/bin/env python3

import random

def main():
    print(random.randrange(1, 10))


if __name__ == "__main__":
    main()
```

`randint` and `seed`

### 7.4. Absolute value

```python
#!/usr/bin/env python3

import random

def main():
    print(abs(-1))


if __name__ == "__main__":
    main()
```

Output:

```shell
1
```

### 7.5. Using the math module

A [math](https://docs.python.org/3/library/math.html) modules ships with Python for advanced calculations.

```python
#!/usr/bin/env python3

import math

def main():
    # print Pi
    print(math.pi)
    # Determine the smallest integer greater than or equal
    print(math.ceil(8.3))
    # Determine the largest integer smaller than or equal
    print(math.floor(8.3))
    # Print the square root
    print(math.sqrt(9))


if __name__ == "__main__":
    main()
```

Output:

```shell
3.141592653589793
9
8
3.0
```

### 7.6. Converting between decimal, binary, octal, and hexadecimal

```python
#!/usr/bin/env python3

import math

def main():
    value_dec = 128
    value_bin = 0b10000000
    value_oct = 0o200
    value_hex = 0x80

    print("The value_decimal value of", value_dec, "is:")
    print(bin(value_dec), "in binary.")
    print(oct(value_dec), "in octal.")
    print(hex(value_dec), "in hexadecimal.")

    print("The binary value of", (value_bin), "is:")
    print(int(value_bin), "in decimal.")
    print(oct(value_bin), "in octal.")
    print(hex(value_bin), "in hexadecimal.")

    print("The octal value of", oct(value_oct), "is:")
    print(int(value_oct), "in decimal.")
    print(bin(value_oct), "in binary.")
    print(hex(value_oct), "in hexadecimal.")

    print("The hexvalue_decimal value of", hex(value_hex), "is:")
    print(int(value_hex), "in decimal.")
    print(bin(value_hex), "in binary.")
    print(oct(value_hex), "in octal.")


if __name__ == "__main__":
    main()
```

Output:

```shell
The value_decimal value of 128 is:
0b10000000 in binary.
0o200 in octal.
0x80 in hexadecimal.
The binary value of 128 is:
128 in decimal.
0o200 in octal.
0x80 in hexadecimal.
The octal value of 0o200 is:
128 in decimal.
0b10000000 in binary.
0x80 in hexadecimal.
The hexvalue_decimal value of 0x80 is:
128 in decimal.
0b10000000 in binary.
0o200 in octal.
```

<!--nextpage-->
## 8. Booleans

### 8.1. The basics about booleans

```python
#!/usr/bin/env python3

def main():
    print(1 > 2)
    print(1 == 2)
    print(1 < 2)
    print(bool(0))
    print(bool(1))


if __name__ == "__main__":
    main()
```

Output:

```shell
False
False
True
False
True
```

```python
#!/usr/bin/env python3

def main():
    x = 10
    y = 5

    if x > y:
        print("x is greater than y")
    else:
        print("x is not greater than y")


if __name__ == "__main__":
    main()
```

Output:

```shell
x is greater than y
```

### 8.2. Some values are false

```python
#!/usr/bin/env python3

class myClass():
    def __len__(self):
        return 0


def main():
    myobj = myClass()
    print(bool(myobj))


if __name__ == "__main__":
    main()
```

Output:

```shell
False
```

### 8.3. Functions can also return a boolean

```python
#!/usr/bin/env python3

def trueFunction():
    return True


def main():
    if trueFunction():
        print("True")
    else:
        print("False")


if __name__ == "__main__":
    main()
```

Output:

```shell
True
```

<!--nextpage-->
## 9. Operators

### 9.1. Arithmetic operators

| Operator | Name           | Example |
| :------: | :------------- | :------ |
|    +     | Addition       | x + y   |
|    -     | Subtraction    | x - y   |
|    *     | Multiplication | x * y   |
|    /     | Division       | x / y   |
|    %     | Modulus        | x % y   |
|    **    | Exponentiation | x ** y  |
|    //    | Floor division | x // y  |

### 9.2. Comparison operators

| Operator | Name                     | Example |
| :------: | :----------------------- | :------ |
|    ==    | Equal                    | x == y  |
|    !=    | Not equal                | x != y  |
|    >     | Greater than             | x > y   |
|    <     | Less than                | x < y   |
|    >=    | Greater than or equal to | x >= y  |
|    <=    | Less than or equal to    | x <= y  |

### 9.3. Logical operators

| Operator | Description                                             | Example               |
| :------: | :------------------------------------------------------ | :-------------------- |
|   and    | Returns True if both statements are true                | x < 5 and  x < 10     |
|    or    | Returns True if one of the statements is true           | x < 5 or x < 4        |
|   not    | Reverse the result, returns False if the result is true | not(x < 5 and x < 10) |

### 9.4. Identity operators

| Operator | Description                                            | Example    |
| :------: | :----------------------------------------------------- | :--------- |
|    is    | Returns True if both variables are the same object     | x is y     |
|  is not  | Returns True if both variables are not the same object | x is not y |

### 9.5. Membership operators

| Operator | Description                                                                      | Example    |
| :------: | :------------------------------------------------------------------------------- | :--------- |
|    in    | Returns True if a sequence with the specified value is present in the object     | x in y     |
|  not in  | Returns True if a sequence with the specified value is not present in the object | x not in y |

### 9.6. Bitwise operators

| Operator | Name                 | Description                                                                                             |
| :------: | :------------------- | :------------------------------------------------------------------------------------------------------ |
|    &     | AND                  | Sets each bit to 1 if both bits are 1                                                                   |
|    \|    | OR                   | Sets each bit to 1 if one of two bits is 1                                                              |
|    ^     | XOR                  | Sets each bit to 1 if only one of two bits is 1                                                         |
|    ~     | NOT                  | Inverts all the bits                                                                                    |
|    <<    | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off                        |
|    >>    | Signed right shift   | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |

### 9.7. Assignment operators

| Operator | Description               | Example | Long form  |
| :------: | :------------------------ | :------ | :--------- |
|    =     | Assignment                | x = 2   | x = 2      |
|    +=    | Arithmetic Addition       | x += 2  | x = x + 2  |
|    -=    | Arithmetic Subtraction    | x -= 2  | x = x - 2  |
|    *=    | Arithmetic Multiplication | x *= 2  | x = x * 2  |
|    /=    | Arithmetic Division       | x /= 2  | x = x / 2  |
|    %=    | Arithmetic Modulus        | x %= 2  | x = x % 2  |
|   //=    | Arithmetic Exponentiation | x //= 2 | x = x // 2 |
|   **=    | Arithmetic Floor division | x **= 2 | x = x ** 2 |
|    &=    | Bitwise AND               | x &= 2  | x = x & 2  |
|   \|=    | Bitwise OR                | x \|= 2 | x = x \| 2 |
|    ^=    | Bitwise XOR               | x ^= 2  | x = x ^ 2  |
|   >>=    | Bitwise Shift Left        | x >>= 2 | x = x >> 2 |
|   <<=    | Bitwise Shift Right       | x <<= 2 | x = x << 2 |

<!--nextpage-->
## 10. Python Collections

There are four collection data types in the Python programming language:

- **List** is a collection which is ordered and changeable. Allows duplicate members
- **Tuple** is a collection which is ordered and unchangeable. Allows duplicate members.
- **Set** is a collection which is unordered and unindexed. No duplicate members.
- **Dictionary** is a collection which is ordered* and changeable. No duplicate members.

### 10.1. Lists

Lists are used to store multiple items in a single variable.

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    print(mylist)


if __name__ == "__main__":
    main()
```

Output

```shell
['apple', 'banana', 'cherry']
```

Lists can have duplicates and are ordered

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry", "apple", "cherry"]
    print(mylist)


if __name__ == "__main__":
    main()
```

List length `len()`

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    print(len(mylist))


if __name__ == "__main__":
    main()
```

A lists can contain different data types

```python
#!/usr/bin/env python3

def main():
    mylist1 = ["apple", "banana", "cherry"]
    mylist2 = [1, 5, 7, 9, 3]
    mylist3 = [True, False, False]
    mylist4 = ["abc", 34, True, 40, "male"]

    print(mylist1)
    print(mylist2)
    print(mylist3)
    print(mylist4)


if __name__ == "__main__":
    main()
```

Using the type() function

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    print(type(mylist))


if __name__ == "__main__":
    main()
```

```shell
<class 'list'>
```

Uusing the list() constructor

```python
#!/usr/bin/env python3

def main():
    mylist = list(("apple", "banana", "cherry"))
    print(mylist)


if __name__ == "__main__":
    main()
```

List items can directly be addressed

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    print(mylist[1])


if __name__ == "__main__":
    main()
```

Output:

```shell
banana
```

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    print(mylist[-1])


if __name__ == "__main__":
    main()
```

Output:

```shell
cherry
```

Indexes

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[2:5])


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[:4])
```

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[2:])


if __name__ == "__main__":
    main()
```

Negative indexes

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[-4:-1])


if __name__ == "__main__":
    main()
```

Check if item exists

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    if "apple" in mylist:
        print("Yes, 'apple' is in the fruits list")


if __name__ == "__main__":
    main()
```

Changing an item

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist[1] = "blackcurrant"
    print(mylist)


if __name__ == "__main__":
    main()
```

Changing a range of items

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
    mylist[1:3] = ["blackcurrant", "watermelon"]
    print(mylist)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
    mylist[1:2] = ["blackcurrant", "watermelon"]
    print(mylist)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist[1:3] = ["watermelon"]
    print(mylist)


if __name__ == "__main__":
    main()
```

Append an item

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.append("orange")
    print(mylist)


if __name__ == "__main__":
    main()
```

Insert items

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.insert(2, "watermelon")
    print(mylist)


if __name__ == "__main__":
    main()
```

Extending a list

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    tropical = ["mango", "pineapple", "papaya"]
    mylist.extend(tropical)
    print(mylist)


if __name__ == "__main__":
    main()
```

Adding

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mytuple = ("kiwi", "orange")
    mylist.extend(mytuple)
    print(mylist)


if __name__ == "__main__":
    main()
```

Remove a specified item

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.remove("banana")
    print(mylist)


if __name__ == "__main__":
    main()
```

Remove a specified index item

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.pop(1)
    print(mylist)


if __name__ == "__main__":
    main()
```

Remove the last item

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.pop()
    print(mylist)


if __name__ == "__main__":
    main()
```

Remove the first item

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    del mylist[0]
    print(mylist)


if __name__ == "__main__":
    main()
```

Delete the entire list

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    del mylist


if __name__ == "__main__":
    main()
```

Clear the list

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.clear()
    print(mylist)


if __name__ == "__main__":
    main()
```

Sort the list

```python
#!/usr/bin/env python3

def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.sort()
    print(mylist)


if __name__ == "__main__":
    main()
```

### 10.2. Tuples

Tuples are used to store multiple items in a single variable, and are ordered, allow duplicates

```python
def main():
    mytuple = ("apple", "banana", "cherry", "apple")
    print(mytuple)
```

Output

```shell
('apple', 'banana', 'cherry', 'apple')
```

The number of itmem in a tuple

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    print(len(mytuple))
```

Output

```shell
4
```

Determining the type

```python
def main():
    mytuple = ("apple")
    print(type(mytuple))
    mytuple = ("apple",)
    print(type(mytuple))
```

Output

```shell
<class 'str'>
<class 'tuple'>
```

Creating a tuple using the constructor

```python
def main():
    mytuple = tuple(("apple", "banana", "cherry"))
    print(mytuple)
```

```shell
('apple', 'banana', 'cherry')
```

Accessing items

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    print(mytuple[1])
    print(mytuple[:1])
    print(mytuple[1:])
    print(mytuple[:-1])
```

Check if an item exist in a tuple

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    if "apple" in mytuple:
        print("The apple is in mytuple")
```

Adding an item

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    a = list(mytuple)
    a.append("cherry")
    mytuple = tuple(a)
    print(mytuple)
```

Updating an item

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    a = list(mytuple)
    a[1] = "cherry"
    mytuple = tuple(a)
    print(mytuple)
```

Remove an item

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    a = list(mytuple)
    a.remove("apple")
    mytuple = tuple(a)
    print(mytuple)
```

Unpack a tuple

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    (a, b, c) = mytuple
    print(a)
    print(b)
    print(c)
```

Unpack a tuple with an asterix

```python
def main():
    mytuple = ("apple", "banana", "cherry", "orange", "lemon")
    (a, b, c*) = mytuple
    print(a)
    print(b)
    print(c)
    (a, b*, c) = mytuple
    print(a)
    print(b)
    print(c)
```

Looping through a tuple

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    for a in mytuple:
        print(a)

    for i in range(len(mytuple)):
        print(mytuple[i])

    i = 0
    while i < len(mytuple):
        print(mytuple[i])
        i = i + 1
```

Joining tuples

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    myothertuple = ("orange", "lemon")
    myfulltuple = mytuple + myothertuple
    print(myfulltuple)
```

```python
def main():
    mytuple = ("apple", "banana", "cherry")
    myfulltuple = mytuple * 2
    print(myfulltuple)
```

### 10.3. Sets

Sets are used to store multiple items in a single variable similar to lists, but doesn't allow for duplicates in the set.

```python
def main():
    myset = {"apple", "banana", "cherry", "apple"}
    print(myset)
```

The number of items in a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    print(len(myset))
```

Which type is set?

```python
def main():
    myset = {"apple", "banana", "cherry"}
    print(type(myset))
```

Using the constructor for sets

```python
def main():
    myset = set(("apple", "banana", "cherry"))
    print(type(myset))
```

Add an item to a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    print(myset)
    myset.append("peach")
    print(myset)
```

Add a set to a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = {"peach", "strawberry"}
    print(myset)
    myset.update(myotherset)
    print(myset)
```

Add any iterable to a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = ["peach", "strawberry"]
    print(myset)
    myset.update(myotherset)
    print(myset)
```

Removing an existing item from a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myset.remove("banana")
    print(myset)
```

Removing an possible existing item from a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myset.discard("peach")
    print(myset)
```

Removing the last item from a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myset.pop()
    print(myset)
```

Make the set empty

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myset.clear()
    print(myset)
```

Delete a set

```python
def main():
    myset = {"apple", "banana", "cherry"}
    del myset
    print(myset)
```

Looping

```python
def main():
    myset = {"apple", "banana", "cherry"}
    for a in myset:
        print(a)
```

Joining sets with an union

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = {"peach", "strawberry"}
    myfullset = myset.union(myotherset)
    print(myfullset)
```

Merging a set into a sets

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = {"peach", "strawberry"}
    myset.update(myotherset)
    print(myset)
```

Update a set to keep only duplicates

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = {"apple", "peach", "strawberry"}
    myset.intersection_update(myotherset)
    print(myset)
```

Create a set to with only duplicates

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = {"apple", "peach", "strawberry"}
    deltaset = myset.intersection(myotherset)
    print(deltaset)
```

Update a set to keep all non-duplicates

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = {"apple", "peach", "strawberry"}
    myset.symmetric_difference_update(myotherset)
    print(myset)
```

Create a set to with all non-duplicates

```python
def main():
    myset = {"apple", "banana", "cherry"}
    myotherset = {"apple", "peach", "strawberry"}
    deleaset = myset.symmetric_difference(myotherset)
    print(deltaset)
```

### 10.4. Dictionaries

Dictionaries are used to store values in key-value pairs. As of Python 3.7 dictionaries are ordered, and earlier Python versions are unordered. Also dictionaries are changable.

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    print(mydict)
```

Accessing an item

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    print(mydict["john"])
```

Dictionaries cannot have two items with the same key:

```python
def main():
    mydict = {
        "jack": "apple",
        "jack": "cherry",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    print(mydict)
```

Determine the amount of items in a dictionary

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    print(len(mydict))
```

Data type within Python

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    print(type(mydict))
```

```shell
<class 'dict'>
```

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    print(mydict)
```

Retrieve a value based on the key

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    a = mydict["jonn"]
    print(a)
```

Retrieve a value based on the key with the `get()` method.

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    a = mydict.get("jonn")
    print(a)
```

Retrieve all the keys

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    b = mydict.keys()
    print(b)
```

Updating the dictionary will also update view on list of keys that was retrieved

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    b = mydict.keys()
    print(b)
    mydict["jane"] = "cherry"
    print(b)
```

Retrieve all the values

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    c = mydict.values()
    print(c)
```

Updating the dictionary will also update view on list of values that was retrieved

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    c = mydict.values()
    print(c)
    mydict["jim"] = "cherry"
    mydict["jane"] = "cherry"
    print(c)
```

Retrieve all the items

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    d = mydict.items()
    print(d)
```

Updating the dictionary will also update view on list of items that was retrieved

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    c = mydict.items()
    print(c)
    mydict["jim"] = "cherry"
    mydict["jane"] = "cherry"
    print(c)
```

Check if an item exists

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    if "james" in mydict:
        print("James exists")
```

Updating values and if the item doesn't exist the item is created.

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    mydict["jim"] = "cherry"
    print(mydict)
    mydict.update({"jim", "apple"})
    print(mydict)
```

Removing items

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    mydict.pop("jim")
    print(mydict)
    mydict.popitem()
    print(mydict)
    del mydict["john"]
    print(mydict)
    mydict.clear()
    print(mydict)
```

Looping through a dictionary

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    for a in mydict:
        print(a)
    for a in mydict:
        print(mydict[a])
    for a in mydict.values():
        print(a)
    for a in mydict.keys():
        print(a)
    for a, b in mydict.items():
        print(a, b)
```

Copying a dictionary

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    myotherdict = mydict.copy()
    print(myotherdict)
    myotherdict = dict(mydict)
    print(myotherdict)
```

Make a reference of a dictionary

```python
def main():
    mydict = {
        "jack": "apple",
        "john": "banana",
        "james": "apple"
        "jim": "banana"
    }
    myotherdict = mydict
    print(mydict)
    print(myotherdict)
    myotherdict["jane"] = "cherry"
    print(mydict)
    print(myotherdict)
```

Using nested dictionaries

```python
def main():
    mydict = {
        "jack": {
            "food": "apple"
            "drink": "water"
        },
        "john": {
            "food": "banana"
            "drink": "mildk"
        }
    }
    print(mydict)
```

```python
def main():
    order1 = {
        "food": "apple"
        "drink": "water"
    }
    order2 = {
        "food": "banana"
        "drink": "mildk"
    }
    mydict = {
        "jack": order1,
        "john": order2
    }
    print(mydict)
```

### 10.5. Arrays

```python
def main():
    myarray = ["apple", "banana", "cherry"]
    print(myarray)
```

List length `len()`

```python
def main():
    myarray = ["apple", "banana", "cherry"]
    print(len(myarray))
```

Looping an array

```python
def main():
    myarray = ["apple", "banana", "cherry"]
    for a in myarray:
        print(a)
```

Adding an element

```python
def main():
    myarray = ["apple", "banana", "cherry"]
    myarray.append("kiwi")
    print(myarray)
```

Remove the first occurrence of an element

```python
def main():
    myarray = ["apple", "banana", "cherry", "apple"]
    myarray.remove("apple")
    print(myarray)
```

Remove an element of a position

```python
def main():
    myarray = ["apple", "banana", "cherry"]
    myarray.pop(1)
    print(myarray)
```

<!--nextpage-->
## 11. Conditions

Python supports the usual logical conditions from mathematics:

- Equals: `a == b`
- Not Equals: `a != b`
- Less than: `a < b`
- Less than or equal to: `a <= b`
- Greater than: `a > b`
- Greater than or equal to: `a >= b`

```python
a = 33
b = 200
if b > a:
  print("b is greater than a")
```

Indentation

```python
a = 33
b = 200
if b > a:
print("b is greater than a") # you will get an error
```

### 11.1. if-then-elif

```python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```

### 11.2. if-then-else

```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

```python
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```

### 11.3. Nested if-then-else

```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

### 11.4. Logical operators

And

```python
a = 200
b = 33
c = 500
if a > b and c > a:
  print("Both conditions are True")
```

Or

```python
a = 200
b = 33
c = 500
if a > b or a > c:
  print("At least one of the conditions is True")
```

### 11.5. Shorthand and Conditional Expressions

```python
a = 2
b = 330
if a > b: print("a is greater than b")
```

```python
a = 2
b = 330
print("A") if a > b else print("B")
```

Ternary Conditional Operator

```python
a = 2
b = 330
print("A") if a > b else print("B")
```

```python
b = 330
print("A") if a > b else print("=") if a == b else print("B")
```

<!--nextpage-->
## 12. Using Functions

### 12.1. The basics about functions

```python
def my_function():
    print("Hello from a function")
```

```python
def my_function():
    print("Hello from a function")


def main():
    my_function()
```

```python
def my_function(fname):
    print(fname + " Refsnes")


def main():
    my_function("Emil")
    my_function("Tobias")
    my_function("Linus")
```

```python
def my_function(x):
    return 5 * x


def main():
    print(my_function(3))
    print(my_function(5))
    print(my_function(9))
```

```python
def my_function(country = "Norway"):
    print("I am from " + country)


def main():
    my_function("Sweden")
    my_function("India")
    my_function()
    my_function("Brazil")
```

### 12.2. Introduction to Lambda

A lambda function is an anonymous function

Syntax:

```python
lambda arguments : expression
```

```python
#!/usr/bin/env python3

def main():
    x = lambda a : a + 2
    print(x(2))


if __name__ == "__main__":
    main()
```

Output:

```shell
4
```

```python
#!/usr/bin/env python3

def main():
    x = lambda a, b : a + b
    print(x(2, 3))


if __name__ == "__main__":
    main()
```

Output:

```shell
5
```

### 12.3. Using Lambda functions

```python
#!/usr/bin/env python3

def myDouble(x):
    return lambda a : a * x

def main():
    double = myDouble(2)
    print(double(3))
    print(double(4))


if __name__ == "__main__":
    main()
```

Output:

```shell
6
8
```

<!--nextpage-->
## 13. Loops

### 13.1. While loop

```python
#!/usr/bin/env python3

def main():
    i = 1
    while i < 6:
        print(i)
        i += 1


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    i = 1
    while i < 6:
        print(i)
        if i == 3:
            break
        i += 1


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    i = 0
    while i < 6:
        i += 1
        if i == 3:
            continue
        print(i)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    i = 1
    while i < 6:
        print(i)
        i += 1
    else:
        print("i is no longer less than 6")


if __name__ == "__main__":
    main()
```

### 13.2. For loop

```python
#!/usr/bin/env python3

def main():
    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        print(x)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    for x in "banana":
        print(x)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        if x == "banana":
            break
        print(x)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        if x == "banana":
            continue
        print(x)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    for x in range(6):
        print(x)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    for x in range(2, 6):
        print(x)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    for x in range(2, 30, 3):
        print(x)


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    for x in range(6):
        print(x)
    else:
        print("Finally finished!")


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    for x in range(6):
        if x == 3:
            break
        print(x)
    else:
        print("Finally finished!")


if __name__ == "__main__":
    main()
```

```python
#!/usr/bin/env python3

def main():
    adj = ["red", "big", "tasty"]
    fruits = ["apple", "banana", "cherry"]

    for x in adj:
        for y in fruits:
            print(x, y)


if __name__ == "__main__":
    main()
```

<!--nextpage-->
## 14. User Input

- Python 3.6 uses the `input()` method.
- Python 2.7 uses the `raw_input()` method

```python
def main():
    username = input("Enter username:")
    print("Username is: " + username)
```

> Python stops executing when it comes to the `input()` function, and continues when the user has given some input.

<!--nextpage-->
## 15. Exception handling

### 15.1. The basics about exceptions

```python
#!/usr/bin/env python3

def main():
    try:
        print(x)
    except:
        print("An exception occurred")


if __name__ == "__main__":
    main()
```

Output:

```shell
An exception occurred
```

```python
#!/usr/bin/env python3

def main():
    try:
        print(x)
    except SystemError:
        pass


if __name__ == "__main__":
    main()
```

Output:

```shell
Traceback (most recent call last):
  File "/workspaces/learning-python/test1.py", line 11, in <module>
    main()
  File "/workspaces/learning-python/test1.py", line 5, in main
    print(x)
NameError: name 'x' is not defined
```

```python
#!/usr/bin/env python3

def main():
    x = 1
    try:
        print(x)
    except:
        print("System Error")
    else:
        print("Everything fine")


if __name__ == "__main__":
    main()
```

Output:

```shell
1
Everything fine
```

```python
#!/usr/bin/env python3

def main():
    try:
        print(x)
    except:
        print("System Error")
    finally:
        print("The try-except works")


if __name__ == "__main__":
    main()
```

Output:

```shell
System Error
The try-except works
```

### 15.2. Raise an exception

```python
#!/usr/bin/env python3

def main():
    x = 1
    y = 0

    if y == 0:
        raise Exception("Sorry, can not divide by zero")
    else:
        print(x/y)

if __name__ == "__main__":
    main()
```

Output:

```shell
Traceback (most recent call last):
  File "/workspaces/learning-python/test1.py", line 13, in <module>
    main()
  File "/workspaces/learning-python/test1.py", line 8, in main
    raise Exception("Sorry, can not divide by zero")
Exception: Sorry, can not divide by zero
```

```python
#!/usr/bin/env python3

def main():
    x = 1
    y = "zero"

    if not type(y) is int:
        raise TypeError("Only integers are allowed")
    else:
        if y == 0:
            raise Exception("Sorry, can not divide by zero")
        else:
            print(x/y)

if __name__ == "__main__":
    main()
```

```shell
Traceback (most recent call last):
  File "/workspaces/learning-python/test1.py", line 16, in <module>
    main()
  File "/workspaces/learning-python/test1.py", line 8, in main
    raise TypeError("Only integers are allowed")
TypeError: Only integers are allowed
```

<!--nextpage-->
## 16. Working with Files

### 16.1. Syntax

| Attribuut |  Mode  | Description                                                               |
| :-------: | :----: | :------------------------------------------------------------------------ |
|    "r"    |  Read  | Default value. Opens a file for reading, error if the file does not exist |
|    "a"    | Append | Opens a file for appending, creates the file if it does not exist         |
|    "w"    | Write  | Opens a file for writing, creates the file if it does not exist           |
|    "x"    | Create | Creates the specified file, returns an error if the file exists           |
|    "t"    |  Text  | Default value. Text mode                                                  |
|    "b"    | Binary | Binary mode (e.g. images)                                                 |

```python
def main():
    f = open("demofile.txt")
```

```python
def main():
    f = open("demofile.txt", "rt")
```

### 16.2. Reading files

```python
def main():
    f = open("demofile.txt", "r")
    print(f.read())
```

```python
def main():
    f = open("../demofile.txt", "r")
    print(f.read())
```

Read only part of the file

```python
def main():
    f = open("demofile.txt", "r")
    print(f.read(5))
```

Read lines

```python
def main():
    f = open("demofile.txt", "r")
    print(f.readline())
```

```python
def main():
    f = open("demofile.txt", "r")
    print(f.readline())
    print(f.readline())
```

```python
def main():
    f = open("demofile.txt", "r")
    for x in f:
        print(x)
```

### 16.3. Closing

```python
def main():
    f = open("demofile.txt", "r")
    print(f.readline())
    f.close()
```

### 16.4. Writing files

open and read the file after the appending:

```python
def main():
    f = open("demofile2.txt", "a")
    f.write("Now the file has more content!")
    f.close()

    #open and read the file after the appending:
    f = open("demofile2.txt", "r")
    print(f.read())
```

open and read the file after the appending

```python
def main():
    f = open("demofile3.txt", "w")
    f.write("Woops! I have deleted the content!")
    f.close()

    f = open("demofile3.txt", "r")
    print(f.read())
```

### 16.5. Create a new file

"x", "a", "w"

```python
def main():
    f = open("myfile.txt", "x")
```

```python
def main():
    f = open("myfile.txt", "w")
```

### 16.6. Delete a file or folder

```python
import os

def main():
    os.remove("demofile.txt")
```

```python
import os

def main():
    if os.path.exists("demofile.txt"):
    os.remove("demofile.txt")
    else:
    print("The file does not exist")
```

```python
import os

def main():
    os.rmdir("demodir")
```

<!--nextpage-->
## 17. Modules

### 17.1. Using a module

Create a file called `mymodule.py` with the following

```python
def greeting(name):
    print("Hello, " + name)
```

In our main program we can import the module and can call the function defined in the module.

```python
import mymodule

def main():
    mymodule.greeting("John")
```

### 17.2. Using variable in modules

If we extent `mymodule.py` with the following

```python
person = {
  "name": "John",
  "age": 42,
  "country": "Ireland"
}
```

We can now access the variable `person` and use `age` defined within `person`

```python
import mymodule

def main():
    age = mymodule.person["age"]
    print(age)
```

Output:

```shell
42
```

### 17.3. Import from a module

You can also import a certain section from a module

```python
from mymodule import person

def main():
    print(person["age"])
```

### 17.4. Rename a module

We can rename a module during import

```python
import mymodule as abc

def main():
    age = abc.person["age"]
    print(age)
```

### 17.5. Built-in modules

```python
import platform

def main():
    x = platform.system()
    print(x)
```

```python
import platform

def main():
    x = dir(platform)
    print(x)
```

<!--nextpage-->
## 18. Classes

### 18.1. Creating a class and object

```python
class MyClass:
    a = 42

def main():
    myobject = MyClass()
    print(myboject.a)
```

### 18.2. The constructor method

During the instantiation of a class the constructor method is called to initialize the object. In Python the method name `__init__` is reserved for this purpose.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("John", 42)

print(person1.name)
print(person1.age)
```

### 18.3. Define an object method

Object methods are functions that belong to the object and operation withing the context of the current object.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def myfunc(self):
        print("My name is " + self.name)

person1 = Person("John", 42)
person1.myfunc()
```

### 18.4. The self parameter

The `self` parameter is a reference to the current instance of the class and has been specified in [PEP-8][arguments], but isn't a reserved keyword. The name of first argument can be anything you want.

```python
class Person:
    def __init__(abc, name, age):
        abc.name = name
        abc.age = age

    def myfunc(xyz):
        print("My name is " + xyz.name)

person1 = Person("John", 42)
person1.myfunc()
```

### 18.5. Object actions

Modify an object property

```python
person1.age = 40
```

Delete an object property

```python
del person1.age
```

Delete an object

```python
del person1
```

### 18.6. Inheritance

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def myfunc(self):
        print("My name is " + self.name)

class Engineer(Person):
    pass

engineer1 = Engineer("John", 42)
engineer1.myfunc()
```

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def myfunc(self):
        print("My name is " + self.name)

class Engineer(Person):
    def __init__(self, name, age, field):
        Person.__init__(name, age)
        self.field = field

engineer1 = Engineer("John", 42, "Electronics")
engineer1.myfunc()
```

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def myfunc(self):
        print("My name is " + self.name)

class Engineer(Person):
    def __init__(self, name, age, field):
        super().__init__(name, age)
        self.field = field

engineer1 = Engineer("John", 42, "Electronics")
engineer1.myfunc()
```

<!--nextpage-->
## 19. Iterators

An interator is an object that contains a countable number of values and can be interated upon. Every object which implements the interator protocol with methods `__iter__()` and `__next__()`.

### 19.1. The basics about iterators

```python
#!/usr/bin/env python3

def main():
    mytuple = ("red", "big", "tasty")
    myit = iter(mytuple)

    print(next(myit))
    print(next(myit))
    print(next(myit))


if __name__ == "__main__":
    main()
```

```shell
red
big
tasty
```

```python
#!/usr/bin/env python3

def main():
    mystr = "red"
    myit = iter(mystr)

    print(next(myit))
    print(next(myit))
    print(next(myit))


if __name__ == "__main__":
    main()
```

```shell
r
e
d
```

```python
#!/usr/bin/env python3

def main():
    mytuple = ("red", "big", "tasty")

    for x in mytuple:
        print(x)


if __name__ == "__main__":
    main()
```

```shell
red
big
tasty
```

```python
#!/usr/bin/env python3

def main():
    mystr = "red"

    for x in mystr:
        print(x)


if __name__ == "__main__":
    main()
```

```shell
r
e
d
```

### 19.2. Creating an iterator

```python
#!/usr/bin/env python3

class MyCounter:
    def __iter__(self):
        self.i = 1
        return self

    def __next__(self):
        j = self.i
        self.i += 1
        return j


def main():
    mycounter = MyCounter()
    myit = iter(mycounter)

    print(next(myit))
    print(next(myit))
    print(next(myit))
    print(next(myit))


if __name__ == "__main__":
    main()
```

```shell
1
2
3
4
```

```python
#!/usr/bin/env python3

class MyCounter:
    def __iter__(self):
        self.i = 1
        return self

    def __next__(self):
        if self.i <= 5:
            j = self.i
            self.i += 1
            return j
        else:
            raise StopIteration


def main():
    mycounter = MyCounter()
    myit = iter(mycounter)

    for x in myit:
        print(x)


if __name__ == "__main__":
    main()
```

```shell
1
2
3
4
5
```

<!--nextpage-->
## 20. PIP: Using packages and virtual environments

PIP is a package manager for Python for packages or modules

### 20.1. Create and start the virtual environment

First we create virtual environment

```shell
$ python3 -m venv .venv
$
```

To activate the

```shell
$ source .venv/bin/activate
(.venv) $ python
Python 3.9.2 (default, Feb 20 2021, 00:00:00) 
[GCC 10.2.1 20201125 (Red Hat 10.2.1-9)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import sys
>>> sys.path
['', '/usr/lib64/python39.zip', '/usr/lib64/python3.9', '/usr/lib64/python3.9/lib-dynload', '/workspaces/python-examples/.venv/lib64/python3.9/site-packages', '/workspaces/python-examples/.venv/lib/python3.9/site-packages']
>>>
```

### 20.2. Managing packages with pip

Since Python 3.4, Pip is installed by default en

```shell
$ source .venv/bin/activate
(.venv) $ python -m pip search camelcase
```

```shell
$ source .venv/bin/activate
(.venv) $ pip search camelcase
```

```shell
(.venv) $ pip install camelcase
Collecting camelcase
  Using cached camelcase-0.2.tar.gz (1.3 kB)
Using legacy 'setup.py install' for camelcase, since package 'wheel' is not installed.
Installing collected packages: camelcase
    Running setup.py install for camelcase ... done
Successfully installed camelcase-0.2
```

```shell
(.venv) $ pip install camelcase==0.1
Collecting camelcase==0.1
  Downloading camelcase-0.1.tar.gz (1.2 kB)
Using legacy 'setup.py install' for camelcase, since package 'wheel' is not installed.
Installing collected packages: camelcase
  Attempting uninstall: camelcase
    Found existing installation: camelcase 0.2
    Uninstalling camelcase-0.2:
      Successfully uninstalled camelcase-0.2
    Running setup.py install for camelcase ... done
Successfully installed camelcase-0.1
```

```shell
(.venv) $ pip install --upgrade camelcase
Collecting camelcase
  Using cached camelcase-0.2.tar.gz (1.3 kB)
Using legacy 'setup.py install' for camelcase, since package 'wheel' is not installed.
Installing collected packages: camelcase
  Attempting uninstall: camelcase
    Found existing installation: camelcase 0.1
    Uninstalling camelcase-0.1:
      Successfully uninstalled camelcase-0.1
    Running setup.py install for camelcase ... done
Successfully installed camelcase-0.2
```

```shell
(.venv) $ pip show camelcase
Name: camelcase
Version: 0.2
Summary: Converts a string to Camel Case
Home-page: http://www.craigaddyman.com
Author: Craig Addyman
Author-email: craig.addyman@googlemail.com
License: MIT
Location: /workspaces/python-examples/.venv/lib/python3.9/site-packages
Requires: 
Required-by:
```

```shell
(.venv) $ pip list
Package    Version
---------- -------
camelcase  0.2
pip        20.2.2
setuptools 49.1.3
```

### 20.3. Install all dependencies

```shell
(.venv) $ pip freeze > requirements.txt
(.venv) $ cat requirements.txt
camelcase==0.2
```

```shell
(.venv) $ pip uninstall camelcase
Found existing installation: camelcase 0.2
Uninstalling camelcase-0.2:
  Would remove:
    /workspaces/python-examples/.venv/lib/python3.9/site-packages/camelcase-0.2-py3.9.egg-info
    /workspaces/python-examples/.venv/lib/python3.9/site-packages/camelcase/*
Proceed (y/n)? y
  Successfully uninstalled camelcase-0.2
```

```shell
(.venv) $ pip install -r requirements.txt
Collecting camelcase==0.2
  Using cached camelcase-0.2.tar.gz (1.3 kB)
Using legacy 'setup.py install' for camelcase, since package 'wheel' is not installed.
Installing collected packages: camelcase
    Running setup.py install for camelcase ... done
Successfully installed camelcase-0.2
```

[black]: https://black.readthedocs.io/en/stable/
[python-devcontainer]: https://github.com/hspaans/python-devcontainer
[python-template]: https://github.com/hspaans/python-template
[vscode]: https://code.visualstudio.com
[vscode-containers]: https://code.visualstudio.com/docs/remote/containers
[vscode-wsl]: https://code.visualstudio.com/docs/remote/wsl
[git-win]: https://git-scm.com/download/win
[PCAP]: https://pythoninstitute.org/certification/pcap-certification-associate/
[PCEP]: https://pythoninstitute.org/certification/pcep-certification-entry-level/
[Python]: https://www.python.org/
[PCPP]: https://pythoninstitute.org/certification/pcpp-certification-professional/
[arguments]: https://www.python.org/dev/peps/pep-0008/#function-and-method-arguments
[shebang]: https://en.m.wikipedia.org/wiki/Shebang_(Unix)
[pep-0008]: https://www.python.org/dev/peps/pep-0008/
[pep-0257]: https://www.python.org/dev/peps/pep-0257/
[stackoverflow-2504411]: https://stackoverflow.com/questions/2504411/proper-indentation-for-python-multiline-strings
