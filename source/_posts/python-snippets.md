---
title: "Python snippets"
date: 2014-12-11 16:55:24
categories:
- comp.lang
tags:
- python
- snippets
toc: true
---

> TODO: add code from `~/wip/python-example/`

## loop files in folder

[Python: List Files in a Directory](http://stackabuse.com/python-list-files-in-a-directory/)

```python
import os
for root, dirs, files in os.walk("/mydir"):
    for file in files:
        if file.endswith(".txt"):
            print(os.path.join(root, file))
```

```python
import pathlib

# define the path
currentDirectory = pathlib.Path('.')

# define the pattern
currentPattern = "*.txt"

for currentFile in currentDirectory.glob(currentPattern):
    print(currentFile)
```

## CSV

[14.1. csv — CSV File Reading and Writing — Python 3 documentation](https://docs.python.org/3/library/csv.html)

[Reading and Writing CSV Files in Python – Real Python](https://realpython.com/python-csv/)
[Reading and Writing CSV Files in Python](http://stackabuse.com/reading-and-writing-csv-files-in-python/)

## RLE

Run length encode with `itertools.groupby()`

```py
from itertools import groupby 
[(c,len(list(cs))) for c,cs in groupby(string)]
```

## Natural sort

[Sorting for Humans : Natural Sort Order](https://blog.codinghorror.com/sorting-for-humans-natural-sort-order/)
[sorting - Does Python have a built in function for string natural sort? - Stack Overflow](https://stackoverflow.com/questions/4836710/does-python-have-a-built-in-function-for-string-natural-sort)

```python
import re

def natural_sort(l):
    def convert(text): return int(text) if text.isdigit() else text.lower()

    def alphanum_key(key): return [convert(c)
                                   for c in re.split('([0-9]+)', key)]
    return sorted(l, key=alphanum_key)
```

## FourCC


```python
import struct

def encode_fourcc(fourcc):
    return struct.unpack("!I", fourcc.encode('ascii'))[0]

def decode_fourcc(v):
    return struct.pack("!I", v).decode("ascii")
```

## find duplicates in list

```python
l = [ 1, 2, 3, 4, 3, 1]

if len(set(l)) != len(l):
    s = set()
    print(
        "Duplicates",
        set(x for x in l if x in s or s.add(x)))
```

## http server

```sh
python2 -m SimpleHTTPServer 8000
python3 -m http.server 8000
```

## test network

```python
import socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect(('mariadb', 3306))
s.recv(1024)
```

```python
import socket
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.connect(('10.6.64.48', 80))
s.send('GET / HTTP/1.1\nHost: 10.6.64.48\n\n')
s.recv(1024)
```

## Random number

[Generating Random Data in Python (Guide) – Real Python](https://realpython.com/python-random/)
[Fastest way to generate a random-like unique string with random length in Python 3 - Stack Overflow](https://stackoverflow.com/questions/48421142/fastest-way-to-generate-a-random-like-unique-string-with-random-length-in-python/48421303#48421303)

[9.6. random — Generate pseudo-random numbers — Python 3 documentation](https://docs.python.org/3/library/random.html)
[15.3. secrets — Generate secure random numbers for managing secrets — Python 3 documentation](https://docs.python.org/3/library/secrets.html)
[16.1. os.urandom() — Miscellaneous operating system interfaces — Python 3 documentation](https://docs.python.org/3/library/os.html#os.urandom)
[22.20. uuid — UUID objects according to RFC 4122 — Python 3 documentation](https://docs.python.org/3/library/uuid.html)
