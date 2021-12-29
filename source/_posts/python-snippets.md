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

## Site package

[installation - How do I find the location of my Python site-packages directory? - Stack Overflow](https://stackoverflow.com/questions/122327/how-do-i-find-the-location-of-my-python-site-packages-directory)

```sh
python -m site
python -c 'import site; print(site.getsitepackages())'
```

## clipping

```python
def clip(n, smallest, largest): return max(smallest, min(n, largest))
```

## loop files in folder

[Python: List Files in a Directory](http://stackabuse.com/python-list-files-in-a-directory/)

```python
import os
for root, dirs, files in os.walk("."):
    for file in files:
        if file.endswith(".py"):
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

## Flatten list

[Fastest Way to Flatten a List in Python - Chris Conlan](https://chrisconlan.com/fastest-way-to-flatten-a-list-in-python/)

```python
a += b
```

## CSV

[14.1. csv — CSV File Reading and Writing — Python documentation](https://docs.python.org/3/library/csv.html)

[Reading and Writing CSV Files in Python – Real Python](https://realpython.com/python-csv/)
[Reading and Writing CSV Files in Python](http://stackabuse.com/reading-and-writing-csv-files-in-python/)

```python
# extra noise needed for this script to work in Windows and
# create Excel readable CSV
import csv

with open(filepath, "w", newline="", encoding="utf-8") as fp:
    fp.write("\ufeff")  #  BOM
    writer = csv.writer(fp)
    writer.writerow(HEADER)
    writer.writerow(ROW)
```

## groupby

```python
# key by id, values are item
# for dict items use `itemgetter("id")`
from itertools import groupby
from operator import itemgetter
labelsById = {
    key: next(groupiter)
    for key, groupiter in groupby(
        labels, key=itemgetter("id")
    )
}

# group by id, values are lists of items
# for class items use `getattr(object, "id")`")`
from itertools import groupby
labelsById = {
    key: list(groupiter)
    for key, groupiter in groupby(
        labels, key=lambda l: getattr(l, "id")
    )
}

```

## sort

```python
# this creates a new list
# for dict items use `itemgetter("id")`
from operator import itemgetter
sorted(dicts, key=itemgetter("id"))

# this modify list in place
# for class items use `getattr(object, "id")`")`
sort(classes, key=lambda l: getattr(l, "id"))
```

## sort dict

```python
people = [
    { 'name': 'John', "age": 64 },
    { 'name': 'Janet', "age": 34 },
    { 'name': 'Ed', "age": 24 },
    { 'name': 'Sara', "age": 64 },
    { 'name': 'John', "age": 32 },
    { 'name': 'Jane', "age": 34 },
    { 'name': 'John', "age": 99 },
]

import operator
people.sort(key=operator.itemgetter('age'))
people.sort(key=operator.itemgetter('name'))

[
    {'name': 'Ed',   'age': 24},
    {'name': 'Jane', 'age': 34},
    {'name': 'Janet','age': 34},
    {'name': 'John', 'age': 32},
    {'name': 'John', 'age': 64},
    {'name': 'John', 'age': 99},
    {'name': 'Sara', 'age': 64}
]
```

## group_adjacent

```python
a = [1, 2, 3, 4, 5, 6]
group_adjacent = lambda a, k: zip(*([iter(a)] * k))
group_adjacent(a, 3) [(1, 2, 3), (4, 5, 6)]
group_adjacent(a, 2) [(1, 2), (3, 4), (5, 6)]
group_adjacent(a, 1)
```

## bail

```python
import sys

def bail(msg: str):
    print(msg, file=sys.stderr)
    exit(1)
```

## JSON

```python
import json
import os

def json_load(infile: os.PathLike, **kwargs) -> dict:
    """load JSON file specified by `infile` as `dict`"""
    with open(infile, encoding="utf-8") as fp:
        return json.load(fp, **kwargs)

def json_dump(data: dict, outfile: os.PathLike, minify: bool = False, **kwargs):
    """save `data` as JSON file to path specified by `outfile`"""
    with open(outfile, "w", encoding="utf-8") as fp:
        if minify:
            json.dump(
                data, fp, separators=(",", ":"), ensure_ascii=False, skipkeys=True, **kwargs
            )
        else:
            json.dump(data, fp, indent=2, ensure_ascii=False, skipkeys=True, **kwargs)
```

## Lodash

[pydash — pydash documentation](https://pydash.readthedocs.io/en/latest/)

```python
# _.pick()
newdict = {k: v for k, v in olddict.items() if k.startswith("foo")}
newdict = {k: v for k, v in olddict.items() if k in ["a", "b", "c"]}
```

## RLE

Run length encode with `itertools.groupby()`

```python
from itertools import groupby
[(c,len(list(cs))) for c,cs in groupby(string)]
```

## Natural sort

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

```python
import socket

ais = socket.getaddrinfo("www.yahoo.com",0,0,0,0)
ip_list = list({addr[-1][0] for addr in ais})
```

```python
#!/usr/bin/python3
# -*- coding: utf-8 -*-
# Technical support: https://www.jianshu.com/u/69f40328d4f0
# Technical support https://china-testing.github.io/
# https://github.com/china-testing/python-api-tesing/blob/master/practices/ping.py
# Discuss nail free group 21745728 qq q group 144081101 567351477
# CreateDate: 2018-11-22

import os
import argparse
import socket
import struct
import select
import time


ICMP_ECHO_REQUEST = 8  # Platform specific
DEFAULT_TIMEOUT = 2
DEFAULT_COUNT = 4


class Pinger(object):
    """ Pings to a host -- the Pythonic way"""

    def __init__(self, target_host, count=DEFAULT_COUNT, timeout=DEFAULT_TIMEOUT):
        self.target_host = target_host
        self.count = count
        self.timeout = timeout

    def do_checksum(self, source_string):
        """  Verify the packet integritity """
        sum = 0
        max_count = (len(source_string) / 2) * 2
        count = 0
        while count < max_count:

            val = source_string[count + 1] * 256 + source_string[count]
            sum = sum + val
            sum = sum & 0xFFFFFFFF
            count = count + 2

        if max_count < len(source_string):
            sum = sum + ord(source_string[len(source_string) - 1])
            sum = sum & 0xFFFFFFFF

        sum = (sum >> 16) + (sum & 0xFFFF)
        sum = sum + (sum >> 16)
        answer = ~sum
        answer = answer & 0xFFFF
        answer = answer >> 8 | (answer << 8 & 0xFF00)
        return answer

    def receive_pong(self, sock, ID, timeout):
        """
        Receive ping from the socket.
        """
        time_remaining = timeout
        while True:
            start_time = time.time()
            readable = select.select([sock], [], [], time_remaining)
            time_spent = time.time() - start_time
            if readable[0] == []:  # Timeout
                return

            time_received = time.time()
            recv_packet, addr = sock.recvfrom(1024)
            icmp_header = recv_packet[20:28]
            type, code, checksum, packet_ID, sequence = struct.unpack(
                "bbHHh", icmp_header
            )
            if packet_ID == ID:
                bytes_In_double = struct.calcsize("d")
                time_sent = struct.unpack("d", recv_packet[28 : 28 + bytes_In_double])[
                    0
                ]
                return time_received - time_sent

            time_remaining = time_remaining - time_spent
            if time_remaining <= 0:
                return

    def send_ping(self, sock, ID):
        """
        Send ping to the target host
        """
        target_addr = socket.gethostbyname(self.target_host)

        my_checksum = 0

        # Create a dummy heder with a 0 checksum.
        header = struct.pack("bbHHh", ICMP_ECHO_REQUEST, 0, my_checksum, ID, 1)
        bytes_In_double = struct.calcsize("d")
        data = (192 - bytes_In_double) * "Q"
        data = struct.pack("d", time.time()) + bytes(data.encode("utf-8"))

        # Get the checksum on the data and the dummy header.
        my_checksum = self.do_checksum(header + data)
        header = struct.pack(
            "bbHHh", ICMP_ECHO_REQUEST, 0, socket.htons(my_checksum), ID, 1
        )
        packet = header + data
        sock.sendto(packet, (target_addr, 1))

    def ping_once(self):
        """
        Returns the delay (in seconds) or none on timeout.
        """
        icmp = socket.getprotobyname("icmp")
        sock = socket.socket(socket.AF_INET, socket.SOCK_RAW, icmp)

        my_ID = os.getpid() & 0xFFFF

        self.send_ping(sock, my_ID)
        delay = self.receive_pong(sock, my_ID, self.timeout)
        sock.close()
        return delay

    def ping(self):
        """
        Run the ping process
        """
        for i in range(self.count):
            print("Ping to %s..." % self.target_host)
            try:
                delay = self.ping_once()
            except socket.gaierror as e:
                print("Ping failed. (socket error: '%s')" % e[1])
                break

            if delay == None:
                print("Ping failed. (timeout within %ssec.)" % self.timeout)
            else:
                delay = delay * 1000
                print("Get pong in %0.4fms" % delay)


if __name__ == "__main__":
    parser = argparse.ArgumentParser(description="Python ping")
    parser.add_argument("host", action="store", help=u"host name")
    given_args = parser.parse_args()
    target_host = given_args.host
    pinger = Pinger(target_host=target_host)
    pinger.ping()
```

## Random number

[Generating Random Data in Python (Guide) – Real Python](https://realpython.com/python-random/)
[Fastest way to generate a random-like unique string with random length in Python 3 - Stack Overflow](https://stackoverflow.com/questions/48421142/fastest-way-to-generate-a-random-like-unique-string-with-random-length-in-python/48421303#48421303)

[9.6. random — Generate pseudo-random numbers — Python documentation](https://docs.python.org/3/library/random.html)
[15.3. secrets — Generate secure random numbers for managing secrets — Python documentation](https://docs.python.org/3/library/secrets.html)
[16.1. os.urandom() — Miscellaneous operating system interfaces — Python documentation](https://docs.python.org/3/library/os.html#os.urandom)
[22.20. uuid — UUID objects according to RFC 4122 — Python documentation](https://docs.python.org/3/library/uuid.html)
