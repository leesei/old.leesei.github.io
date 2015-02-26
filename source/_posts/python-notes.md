title: Python notes
toc: true
date: 2014-12-11 16:55:24
tags:
- python
- notes
---

All python code are executed statements, no such thing as declaration

## Terminology

Python     | Java
------     | ----
object     | Object
type       | Class
attributes | member/field
try-except-raise | try-catch-throw

> c.f. JavaScript objects are inherently dict, non-local declarations are made global

## Builtin types

- `list []`: mutable
- `tuple ()`: immutable, `()`` are _optional_
- `dict {}`: map of key, value pairs
- `set(list)`: un-ordered collection of unique items in list
- `zip(lists)`: return the columns of matrix formed using the lists as row

`is` operator test id() of objects
`type` and `object` are instances of each other and themselves
module objects represents `.py` files, created by `import`, each global variables in file added as attributes

## Functions

http://agiliq.com/blog/2012/06/understanding-args-and-kwargs/
http://docs.python.org/2/glossary.html#term-parameter

### Parameters

- positional parameter: `a`
- keyword parameter: `b=default`
- variable positional parameter: `*args`
- variable keyword parameter: `**kwargs`

### Calling

arguments can always be passes as keyword arguments regardless of their definition
`*list`/`*tuple` can unpack list/tuple as positional arguments  
`**dict` can unpack dict as keyword arguments  

### Default for mutable parameter

Function parameter are attributes of function object instance
Default value is only applied upon function definition

```python
def foo(a, b=[]):  # wrong
    b.append(a)
    print a b

def foo(a, b=None):  # correct
    if b is None: b = []
    b.append(a)
    print a b
```

## Namespace

Only functions, class and modules create namespaces

### Assignment (lvalue)

if object not found in local scope, creates it
use `nonlocal` (enclosed)/`global` keywords to override

### Reference (rvalue/function)

**LEGB**: Local -> Enclosed -> Global -> Builtin
need `nonlocal`/`global` keywords when referencing non-local variables

## Classes

Inherit classes from object to signal usage of new style classes
Avoid multiple inheritance with exception to mix-ins (for non-overridden functions not representing IS-A relationship)
Use `@property` declaration to abstract member access (simpler then `__getattribute__`/`__setattr__`)

## Arithmetic

```python
8/3 = 2.666666
8//3 = 2
-8//3.0 = -3 # rounded down!!
```

`int(float)` is rounding, use `floor()` for C-like casting
use open delimiters to override indentation rules

## Learn

Python Fundamentals Training
http://www.youtube.com/playlist?list=PL26BA8B9FC33789FF
http://simeonfranklin.com/python-fundamentals/
4 day comprehensive tutorial, target audiences are not advanced

Google Python Class
https://developers.google.com/edu/python/

Python (all parts in one)
http://www.youtube.com/watch?v=Ajmj5itd2s8
quite good

Slightly Advanced Python - Some Python Internals
http://www.youtube.com/watch?v=23s9Wc3aWGY
class contruction, attr lookup, bytecode (assembly)

## Reference

[Overview — Python 3 documentation](https://docs.python.org/3/)
[Overview — Python 2 documentation](https://docs.python.org/2/)
[FrontPage - Python Wiki](https://wiki.python.org/moin/)
[The Hitchhiker’s Guide to Python! — The Hitchhiker's Guide to Python](http://docs.python-guide.org/en/latest/), [source](https://github.com/kennethreitz/python-guide)
[Introduction to Computer Science and Programming Using Python | edX](https://www.edx.org/course/introduction-computer-science-mitx-6-00-1x-0#.VIpwguqUfF4)
[Dive Into Python](http://linux.die.net/diveintopython/html/) (Python 2)
