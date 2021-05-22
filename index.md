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
  - [6.6. Modifying strings](#66-modifying-strings)
    - [6.6.1. Convert your string to upper or lower case](#661-convert-your-string-to-upper-or-lower-case)
    - [6.6.2. Removing a whitespace](#662-removing-a-whitespace)
    - [6.6.3. Replacing a string](#663-replacing-a-string)
    - [6.6.4. Split a string](#664-split-a-string)
  - [6.7. Formatting strings](#67-formatting-strings)
  - [6.8. Escape characters](#68-escape-characters)
- [7. Numbers](#7-numbers)
  - [7.1. The basics about numbers](#71-the-basics-about-numbers)
  - [7.2. Type conversion](#72-type-conversion)
- [8. Python Collections](#8-python-collections)
  - [8.1. Lists](#81-lists)
  - [8.2. Tuples](#82-tuples)
  - [8.3. Sets](#83-sets)
  - [8.4. Dictionaries](#84-dictionaries)
  - [8.5. Arrays](#85-arrays)
- [9. Functions](#9-functions)
  - [9.1. Generate a random number](#91-generate-a-random-number)
  - [9.2. Absolute value](#92-absolute-value)
- [10. Conditions](#10-conditions)
  - [10.1. if-then-elif](#101-if-then-elif)
  - [10.2. if-then-else](#102-if-then-else)
  - [10.3. Nested if-then-else](#103-nested-if-then-else)
  - [10.4. Logical operators](#104-logical-operators)
  - [10.5. Shorthand and Conditional Expressions](#105-shorthand-and-conditional-expressions)
- [11. Using Functions](#11-using-functions)
- [12. Loops](#12-loops)
  - [12.1. While loop](#121-while-loop)
  - [12.2. For loop](#122-for-loop)
- [13. User Input](#13-user-input)
- [14. Exception handling](#14-exception-handling)
- [15. Working with Files](#15-working-with-files)
  - [15.1. Syntax](#151-syntax)
  - [15.2. Reading files](#152-reading-files)
  - [15.3. Closing](#153-closing)
  - [15.4. Writing files](#154-writing-files)
  - [15.5. Create a new file](#155-create-a-new-file)
  - [15.6. Delete a file or folder](#156-delete-a-file-or-folder)
- [16. Modules](#16-modules)
  - [16.1. Using a module](#161-using-a-module)
  - [16.2. Using variable in modules](#162-using-variable-in-modules)
  - [16.3. Import from a module](#163-import-from-a-module)
  - [16.4. Rename a module](#164-rename-a-module)
  - [16.5. Built-in modules](#165-built-in-modules)
- [17. Classes](#17-classes)
  - [17.1. Creating a class and object](#171-creating-a-class-and-object)
  - [17.2. The constructor method](#172-the-constructor-method)
  - [17.3. Define an object method](#173-define-an-object-method)
  - [17.4. The self parameter](#174-the-self-parameter)
  - [17.5. Object actions](#175-object-actions)
  - [17.6. Inheritance](#176-inheritance)
- [18. PIP: Using packages and virtual environments](#18-pip-using-packages-and-virtual-environments)
  - [18.1. Create and start the virtual environment](#181-create-and-start-the-virtual-environment)
  - [18.2. Managing packages with pip](#182-managing-packages-with-pip)
  - [18.3. Install all dependencies](#183-install-all-dependencies)

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

```python
def main:
    phrase_one = "Hello World."
    print(len(phrase_one))
```

### 6.4. Checking a string

```python
def main:
    phrase_one = "Hello World."
    print("Hello" in phrase_one)
```

```python
def main:
    phrase_one = "Hello World."
    if "Hello" in phrase_one:
        print("Yes, Hello World.")
```

```python
def main:
    phrase_one = "Hello World."
    if "Hello" not in phrase_one:
        print("Yes, Hello World.")
```

### 6.5. Slicing strings

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one[2:5])
```

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one[:5])
```

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one[2:])
```

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one[-5:-2])
```

### 6.6. Modifying strings

#### 6.6.1. Convert your string to upper or lower case

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one.upper())
```

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one.lower())
```

#### 6.6.2. Removing a whitespace

```python
def main:
    phrase_one = "Hello World. "
    print(phrase_one.strip())
```

`lstrip` and `rstrip`

#### 6.6.3. Replacing a string

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one.replace("W", "w"))
```

#### 6.6.4. Split a string

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one.split(" "))
```

`join`

### 6.7. Formatting strings

```python
def main:
    name_one = "World"
    phrase_one = "Hello {}."
    print(phrase_one.format(name_one))
```

```python
def main:
    name_one = "Jack"
    name_two = "John"
    phrase_one = "Hello {} and {}."
    print(phrase_one.format(name_one, name_two))
```

```python
def main:
    name_one = "Jack"
    name_two = "John"
    phrase_one = "Hello {1} and {0}."
    print(phrase_one.format(name_one, name_two))
```

### 6.8. Escape characters

```python
def main:
    phrase_one = "Hello "World"."
    print(phrase_one)
```

```python
def main:
    phrase_one = "Hello \"World\"."
    print(phrase_one)
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
def main:
    q = -1
    x = 1
    y = 3.14
    z = 1j
    print(type(q))
    print(type(x))
    print(type(y))
    print(type(z))
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
def main:
    x = 1
    y = 3.14
    z = 1j

    a = float(x)
    b = float(y)

    print(a)
    print(b)

    print(type(a))
    print(type(b))
```

<!--nextpage-->
## 8. Python Collections

There are four collection data types in the Python programming language:

- **List** is a collection which is ordered and changeable. Allows duplicate members
- **Tuple** is a collection which is ordered and unchangeable. Allows duplicate members.
- **Set** is a collection which is unordered and unindexed. No duplicate members.
- **Dictionary** is a collection which is ordered* and changeable. No duplicate members.

### 8.1. Lists

Lists are used to store multiple items in a single variable.

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    print(mylist)
```

Output

```shell
['apple', 'banana', 'cherry']
```

Lists can have duplicates and are ordered

```python
def main():
    mylist = ["apple", "banana", "cherry", "apple", "cherry"]
    print(mylist)
```

List length `len()`

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    print(len(mylist))
```

A lists can contain different data types

```python
def main():
    mylist1 = ["apple", "banana", "cherry"]
    mylist2 = [1, 5, 7, 9, 3]
    mylist3 = [True, False, False]
    mylist4 = ["abc", 34, True, 40, "male"]

    print(mylist1)
    print(mylist2)
    print(mylist3)
    print(mylist4)
```

Using the type() function

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    print(type(mylist))
```

```shell
<class 'list'>
```

Uusing the list() constructor

```python
def main():
    mylist = list(("apple", "banana", "cherry"))
    print(mylist)
```

List items can directly be addressed

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    print(mylist[1])
```

Output:

```shell
banana
```

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    print(mylist[-1])
```

Output:

```shell
cherry
```

Indexes

```python
def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[2:5])
```

```python
def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[:4])
```

```python
def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[2:])
```

Negative indexes

```python
def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(mylist[-4:-1])
```

Check if item exists

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    if "apple" in mylist:
        print("Yes, 'apple' is in the fruits list")
```

Changing an item

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist[1] = "blackcurrant"
    print(mylist)
```

Changing a range of items

```python
def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
    mylist[1:3] = ["blackcurrant", "watermelon"]
    print(mylist)
```

```python
def main():
    mylist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
    mylist[1:2] = ["blackcurrant", "watermelon"]
    print(mylist)
```

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist[1:3] = ["watermelon"]
    print(mylist)
```

Append an item

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.append("orange")
    print(mylist)
```

Insert items

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.insert(2, "watermelon")
    print(mylist)
```

Extending a list

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    tropical = ["mango", "pineapple", "papaya"]
    mylist.extend(tropical)
    print(mylist)
```

Adding

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mytuple = ("kiwi", "orange")
    mylist.extend(mytuple)
    print(mylist)
```

Remove a specified item

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.remove("banana")
    print(mylist)
```

Remove a specified index item

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.pop(1)
    print(mylist)
```

Remove the last item

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.pop()
    print(mylist)
```

Remove the first item

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    del mylist[0]
    print(mylist)
```

Delete the entire list

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    del mylist
```

Clear the list

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.clear()
    print(mylist)
```

Sort the list

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    mylist.sort()
    print(mylist)
```

### 8.2. Tuples

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

### 8.3. Sets

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

### 8.4. Dictionaries

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

### 8.5. Arrays

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
## 9. Functions

### 9.1. Generate a random number

```python
import random

def main:
    print(random.randrange(1, 10))
```

`randint` and `seed`

### 9.2. Absolute value

```python
import random

def main:
    print(abs(-1))
```

<!--nextpage-->
## 10. Conditions

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

### 10.1. if-then-elif

```python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```

### 10.2. if-then-else

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

### 10.3. Nested if-then-else

```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

### 10.4. Logical operators

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

### 10.5. Shorthand and Conditional Expressions

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

## 11. Using Functions

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

<!--nextpage-->
## 12. Loops

### 12.1. While loop

```python
def main():
    i = 1
    while i < 6:
        print(i)
        i += 1
```

```python
def main():
    i = 1
    while i < 6:
        print(i)
        if i == 3:
            break
        i += 1
```

```python
def main():
    i = 0
    while i < 6:
        i += 1
        if i == 3:
            continue
        print(i)
```

```python
def main():
    i = 1
    while i < 6:
        print(i)
        i += 1
    else:
        print("i is no longer less than 6")
```

### 12.2. For loop

```python
def main():
    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        print(x)
```

```python
def main():
    for x in "banana":
        print(x)
```

```python
def main():
    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        if x == "banana":
            break
        print(x)
```

```python
def main():
    fruits = ["apple", "banana", "cherry"]
    for x in fruits:
        if x == "banana":
            continue
        print(x)
```

```python
def main():
    for x in range(6):
        print(x)
```

```python
def main():
    for x in range(2, 6):
        print(x)
```

```python
def main():
    for x in range(2, 30, 3):
        print(x)
```

```python
def main():
    for x in range(6):
        print(x)
    else:
        print("Finally finished!")
```

```python
def main():
    for x in range(6):
        if x == 3:
            break
        print(x)
    else:
        print("Finally finished!")
```

```python
def main():
    adj = ["red", "big", "tasty"]
    fruits = ["apple", "banana", "cherry"]

    for x in adj:
        for y in fruits:
            print(x, y)
```

## 13. User Input

- Python 3.6 uses the `input()` method.
- Python 2.7 uses the `raw_input()` method

```python
def main():
    username = input("Enter username:")
    print("Username is: " + username)
```

> Python stops executing when it comes to the `input()` function, and continues when the user has given some input.

## 14. Exception handling

## 15. Working with Files

### 15.1. Syntax

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

### 15.2. Reading files

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

### 15.3. Closing

```python
def main():
    f = open("demofile.txt", "r")
    print(f.readline())
    f.close()
```

### 15.4. Writing files

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

### 15.5. Create a new file

"x", "a", "w"

```python
def main():
    f = open("myfile.txt", "x")
```

```python
def main():
    f = open("myfile.txt", "w")
```

### 15.6. Delete a file or folder

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
## 16. Modules

### 16.1. Using a module

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

### 16.2. Using variable in modules

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

### 16.3. Import from a module

You can also import a certain section from a module

```python
from mymodule import person

def main():
    print(person["age"])
```

### 16.4. Rename a module

We can rename a module during import

```python
import mymodule as abc

def main():
    age = abc.person["age"]
    print(age)
```

### 16.5. Built-in modules

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

## 17. Classes

### 17.1. Creating a class and object

```python
class MyClass:
    a = 42

def main():
    myobject = MyClass()
    print(myboject.a)
```

### 17.2. The constructor method

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

### 17.3. Define an object method

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

### 17.4. The self parameter

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

### 17.5. Object actions

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

### 17.6. Inheritance

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
## 18. PIP: Using packages and virtual environments

PIP is a package manager for Python for packages or modules

### 18.1. Create and start the virtual environment

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

### 18.2. Managing packages with pip

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

### 18.3. Install all dependencies

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