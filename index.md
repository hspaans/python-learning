---
layout: page
title: Learning Python
toc: true
---

* TOC
{:toc}

## Introduction

[Python][Python] is a language specification with multiple implementations like CPython, Jython, and MicroPython, but almost everyone refers to the CPython implementation as Python that can be found on almost every Linux server. The MicroPython implementation is to run Python on microcontrollers. Jython is the last big implementation of Python 2 that runs on the Java Virtual Machine, but development has mostly stalled, but development for Python 3.8 support has recently started.

The Python Institute also has a certification traject with three levels called [PCEP], [PCAP], and [PCPP]. As the PCAP exam also covers the PCEP objectives most people directly take this exam. The PCPP covers the Python ecosystem part and more advantage architecture patterns.

## Setting up the environment

### Using devcontainers

Learning Python can be done on any system with a text-editor and the Python interpreter. But it is advised to an editor like [Visual Studio Code][vscode] to help you develop your code. Also, VSCode can help you by spinning up a [Python development container][python-devcontainer] in Docker to make sure everything installed and configured correctly everytime.

* Install Git on [Windows][git-win]
* [Setup VSCode](https://code.visualstudio.com/docs/setup/setup-overview)
* [Developing inside a Container](https://code.visualstudio.com/docs/remote/containers)

When you have everything working correctly then [python-template][python-template] repository should start a Python based development container. In the terminal window within VSCode we can start Python manually as below

```shell
vscode@03fdf48d4d7f python-template (master) $ python
Python 3.9.1 (default, Jan 12 2021, 16:56:42) 
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

### Using WSL2

* Install Git on [Windows][git-win]
* [Setup VSCode](https://code.visualstudio.com/docs/setup/setup-overview)
* [Developing in WSL](https://code.visualstudio.com/docs/remote/wsl)

## Your first Python application

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

But what does this all mean? Let start with the first line where tell unix via a [shebang](https://en.m.wikipedia.org/wiki/Shebang_(Unix)) to look the `python3` interpreter via the `env` command. This guarantees that we always find the Python interpreter while we don't set any hardcoded paths. In the [PIP](pip) section we will go deeping into why this important when we start working with virtual environments.

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

## Python syntax

### Indentation

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

```
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

```
  File "/workspaces/python-examples/hello.py", line 7
    print("Hello Jack.")
                        ^
IndentationError: unindent does not match any outer indentation level
```

### Comments

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

```
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

```
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

```
Hello John.
```

## Working with variables

No programs works without variables to store data values in while the program runs. Variables in Python are strong dynamically typed which mean you can change a variable from a number to a string by assignment, but a variable will not become a number when a string contains a number for example. This also means you may have to cast variable from a number to a string in some cases or vice versa.

### The basics

Let start with basic example based on our `Hello World.` application where we have two lines. And in this example we still present print directly with a string telling about two people called John and their age.

```python
def main():
    print("My name is John and I am 42.")
    print("My name is John and I am also 42.")
```

Output:

```
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

```
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

```
My name is John and I am 42.
My name is Jack and I am also 42
```

### Different data types

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

### Casting variables

Python is flexible with its data types for variables, but Python does require type casting in some cases. Using a variable that contains a number that needs to concatenated with a string needs to be casted from an integer to a string. In the example below we forget to type cast a string and it fails.

```python
def main():
    name = "John"
    age = 42
    print("My name is " + name + " and I am " + age + ".")
```

Output:

```
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

### Getting a variable type

Python can also determine the data type of a variable with `type()`. This can become useful when importing data from unknown source and needs validation.

```python
def main():
    name = "John"
    age = 42
    print(type(name))
    print(type(age))
```

Output:

```
<class 'str'>
<class 'int'>
```

### Variable scope

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

```
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

```
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

```
Hello People.
```

> Using global variables is considert bad programming and a risk as it can have unforeseen effects.

## Working with strings

### The basics

The most basic form of a string is one that is given directly to the `print()`

```python
def main:
    print("Hello World.")
```

Output:

```
Hello World.
```

```python
def main:
    phrase_one = "Hello World."
    print(phrase)
```

Output:

```
Hello World.
```

```python
def main:
    phrase_one = "Hello World."
    phrase_two = "And Goodbye."
    print(phrase_one + phrase_two)
```

Output:

```
Hello World.And Goodbye.
```

```python
def main:
    phrase_one = "Hello World."
    phrase_two = "And Goodbye."
    print(phrase_one + " " + phrase_two)
```

Output:

```
Hello World. And Goodbye.
```

```python
def main:
    phrase_one = """Hello World.
    And Goodbye."""
    print(phrase_one)
```

Output:

```
Hello World.
And Goodbye.
```

### Strings are arrays

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one[1])
```

### Looping through a string

```python
def main:
    for x in "Hello World.":
        print(x)
```

### String length

```python
def main:
    phrase_one = "Hello World."
    print(len(phrase_one))
```

### Checking a string

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

### Slicing strings

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

### Modifying strings

#### Convert your string to upper or lower case

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

#### Removing a whitespace


```python
def main:
    phrase_one = "Hello World. "
    print(phrase_one.strip())
```

`lstrip` and `rstrip`

#### Replacing a string

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one.replace("W", "w"))
```

#### Split a string

```python
def main:
    phrase_one = "Hello World."
    print(phrase_one.split(" "))
```

`join`

### Formatting strings

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

### Escape characters

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

## Working with numbers

* `int`
* `float`
* `complex`

### The basics

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

```
<class 'int'>
<class 'int'>
<class 'float'>
<class 'complex'>
```

### Type conversion

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

## Working with Lists

Lists are used to store multiple items in a single variable.

```python
def main():
    alist = ["apple", "banana", "cherry"]
    print(alist)
```

Lists can have duplicates and are ordered

```python
def main():
    alist = ["apple", "banana", "cherry", "apple", "cherry"]
    print(alist)
```

List length `len()`

```python
def main():
    alist = ["apple", "banana", "cherry"]
    print(len(alist))
```

A lists can contain different data types

```python
def main():
    list1 = ["apple", "banana", "cherry"]
    list2 = [1, 5, 7, 9, 3]
    list3 = [True, False, False]
    list4 = ["abc", 34, True, 40, "male"]

    print(list1)
    print(list2)
    print(list3)
    print(list4)
```

Using the type() function

```python
def main():
    mylist = ["apple", "banana", "cherry"]
    print(type(mylist))
```

```
<class 'list'>
```

Uusing the list() constructor

```python
def main():
    alist = list(("apple", "banana", "cherry"))
    print(alist)
```

List items can directly be addressed

```python
def main():
    alist = ["apple", "banana", "cherry"]
    print(alist[1])
```

Output:

```
banana
```

```python
def main():
    alist = ["apple", "banana", "cherry"]
    print(alist[-1])
```

Output:

```
cherry
```

Indexes

```python
def main():
    alist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(alist[2:5])
```


```python
def main():
    alist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(alist[:4])
```

```python
def main():
    alist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(alist[2:])
```

Negative indexes

```python
def main():
    alist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
    print(alist[-4:-1])
```

Check if item exists

```python
def main():
    alist = ["apple", "banana", "cherry"]
    if "apple" in alist:
        print("Yes, 'apple' is in the fruits list")
```

Changing an item

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist[1] = "blackcurrant"
    print(alist)
```

Changing a range of items

```python
def main():
    alist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
    alist[1:3] = ["blackcurrant", "watermelon"]
    print(alist)
```

```python
def main():
    alist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
    alist[1:2] = ["blackcurrant", "watermelon"]
    print(alist)
```

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist[1:3] = ["watermelon"]
    print(alist)
```

Append an item

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist.append("orange")
    print(alist)
```

Insert items

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist.insert(2, "watermelon")
    print(alist)
```

Extending a list

```python
def main():
    alist = ["apple", "banana", "cherry"]
    tropical = ["mango", "pineapple", "papaya"]
    alist.extend(tropical)
    print(alist)
```

Adding

```python
def main():
    alist = ["apple", "banana", "cherry"]
    thistuple = ("kiwi", "orange")
    alist.extend(thistuple)
    print(alist)
```

Remove a specified item

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist.remove("banana")
    print(alist)
```

Remove a specified index item

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist.pop(1)
    print(alist)
```

Remove the last item

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist.pop()
    print(alist)
```

Remove the first item

```python
def main():
    alist = ["apple", "banana", "cherry"]
    del alist[0]
    print(alist)
```

Delete the entire list

```python
def main():
    alist = ["apple", "banana", "cherry"]
    del alist
```

Clear the list

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist.clear()
    print(alist)
```

Sort the list

```python
def main():
    alist = ["apple", "banana", "cherry"]
    alist.sort()
    print(alist)
```

## Working with Sets

## Working with Dictionaries

## Working with Arrays

## Functions

### Generate a random number

```python
import random

def main:
    print(random.randrange(1, 10))
```

`randint` and `seed`

### Absolute value

```python
import random

def main:
    print(abs(-1))
```

## Conditions

Python supports the usual logical conditions from mathematics:

* Equals: `a == b`
* Not Equals: `a != b`
* Less than: `a < b`
* Less than or equal to: `a <= b`
* Greater than: `a > b`
* Greater than or equal to: `a >= b`

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

### if-then-elif

```python
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```

### if-then-else

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

### Nested if-then-else

```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

### Logical operators

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

### Shorthand and Conditional Expressions

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

## Functions

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

## Loops

### While loop

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

### For loop

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

## User Input

* Python 3.6 uses the `input()` method.
* Python 2.7 uses the `raw_input()` method

```python
def main():
    username = input("Enter username:")
    print("Username is: " + username)
```

> Python stops executing when it comes to the `input()` function, and continues when the user has given some input.

## Exception handling

## Working with Files

### Syntax

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

### Reading files

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

### Closing

```python
def main():
    f = open("demofile.txt", "r")
    print(f.readline())
    f.close()
```

### Writing files

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

### Create a new file

"x", "a", "w"

```python
def main():
    f = open("myfile.txt", "x")
```

```python
def main():
    f = open("myfile.txt", "w")
```

### Delete a file or folder

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

## Modules

### Using a module

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

### Using variable in modules

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

```
42
```

### Import from a module

You can also import a certain section from a module

```python
from mymodule import person

def main():
    print(person["age"])
```


### Rename a module

We can rename a module during import

```python
import mymodule as abc

def main():
    age = abc.person["age"]
    print(age)
```

### Built-in modules

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


## Classes

### Creating a class and object

```python
class MyClass:
    a = 42

def main():
    myobject = MyClass()
    print(myboject.a)
```

### The constructor method

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

### Define an object method

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

### The self parameter

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

### Object actions

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

### Inheritance

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

## PIP: Using packages and virtual environments

PIP is a package manager for Python for packages or modules

### Create and start the virtual environment

First we create virtual environment

```shell
$ python3 -m venv .venv
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

### Managing packages with pip

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

### Install all dependencies

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

[python-devcontainer]: https://github.com/hspaans/python-devcontainer
[python-template]: https://github.com/hspaans/python-template
[vscode]: https://code.visualstudio.com
[git-win]: https://git-scm.com/download/win
[PCAP]: https://pythoninstitute.org/certification/pcap-certification-associate/
[PCEP]: https://pythoninstitute.org/certification/pcep-certification-entry-level/
[Python]: https://www.python.org/
[PCPP]: https://pythoninstitute.org/certification/pcpp-certification-professional/
[arguments]: https://www.python.org/dev/peps/pep-0008/#function-and-method-arguments
