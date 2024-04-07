# Chapter 1

## :snake: What is Python? :snake:

Python is a general purpose programming language designed to emphasise readability.

Python uses "significant indentation" - meaning code blocks are differentiated by indentation (tabs or spaces) and not braces ({}). It uses new lines to complete commands as opposed to semicolons.

```python
# a python function
def hello():
    print("hello world")
```

```javascript
// a javascript function
function hello() {
  console.log("hello world");
}
```

Python is dynamically typed meaning an object can be used in any context until it is used in a way that it doesn't support.

This is as opposed to nominative typing where an object is of a given type if it is declared as such.

Python is used for

* web development
* software development
* mathematics
* scripting

It can be run on many platforms; Windows, Mac, Linux etc.

## :new: Getting Started :new:

The following examples can be executed from the Python CLI by opening a terminal and entering `python` or `python3` depending on your installation.

```shell
user@host $ python

Python 3.11.8 (main, Feb 14 2024, 19:11:34) [Clang 15.0.0 (clang-1500.1.0.2.5)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

The CLI can be exited by entering `exit()`.

### Variables

Variables are containers for storing data values. Python has no command for creating a variable, it is created the first time a value is assigned to it. Variables do not need their type specified and can even change type after they have been set.

```shell
>>> name = "John"
>>> print(name)
John
>>> name = 1
>>> print(name)
1
>>> 
```

Values can be cast to types using the type name. There is no implicit casting of types, a type may have limits on the operations that can be applied to it.

```shell
>>> age = str(1)
>>> print(age)
1
>>> age + 1
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
>>> 
```

### Print

As we have seen in the previous examples, values can be output to stdout using the `print` function.

Multiple values can be output by providing them separated by a comma.

```shell
>>> print("Python", "is", "awesome")
Python is awesome
>>>
```

Operations can also be passed to the `print` function with the result being output.

```shell
>>> print(1 + 2)
3
>>> 
```

### Data Types

Variables can store different data types and these can do different things.

Python has the following built in data types:

* Text Type: `str`
* Numeric Types: `int`, `float`, `complex`
* Sequence Types: `list`, `tuple`, `range`
* Mapping Type: `dict`
* Set Types: `set`, `frozenset`
* Boolean Type: `bool`
* Binary Types: `bytes`, `bytearray`, `memoryview`
* None Type: `NoneType`

You can get the data type of a variable using the `type` function.

```shell
>>> name = "John"
>>> type(name)
<class 'str'>
```

You can perform a boolean check on the type with the `isinstance` function. `isinstance` can check against a single type or a union of types separated by a pipe (`|`).

```shell
>>> name = "John"
>>> isinstance(name, str)
True
>>> name = 1
>>> isinstance(name, str)
False
>>> isinstance(name, str | int)
True
>>> name = "John"
>>> isinstance(name, str | int)
True
>>>
```
### Strings

Strings can be defined with either single (`'`) or double (`"`) wuotes.

```shell
>>> "hello" == 'hello'
True
>>> 
```

Multiline strings can be created using three quotes.

```shell
>>> a = """Lorem ipsum dolor sit amet,
... consectetur adipiscing elit,
... sed do eiusmod tempor incididunt
... ut labore et dolore magna aliqua."""
>>> print(a)
Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua.
>>> 
```

As with many coding languages, strings are arrays of bytes. There is no `char` data type in Python so a single character is a string of length `1`.

Because strings are arrays they can be sliced, iterated over, and accessed using an index.

```shell
>>> name = "John"
>>> name[0]
'J'
>>> name[1:]
'ohn'
>>> for i in name:
...     print(i)
... 
J
o
h
n
>>> 
```

The length of a string can be checked using the `len` function.

```shell
>>> len(name)
4
>>> 
```

Substrings can be checked using the `in` keyword.

```shell
>>> name="John Smith"
>>> "Smith" in name
True
>>> 
```
