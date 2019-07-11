---
title: "Shell snippets"
date: 2014-12-08 12:03:44
categories:
- linux
tags:
- shell
- notes
toc: true
---

## `inotifywait`

```sh
#!/bin/bash

test_watch() {
  clear
  inotifywait --quiet --recursive --monitor --format "Changed: %w%f" \
    --event close_write --exclude '(\.sw|~|[[:digit:]]+|node_modules)' \
    . | bin/test;
  test_watch
}

test_watch
```

## test element in array

```sh
# test element in array
in_array()
{
    local hay needle=$1;
    shift;
    for hay in "$@"; do
        echo $hay
        [[ $hay == $needle ]] && return 0;
    done;
    return 1
}
```

## test logic expression

```sh
Test()
{
    eval "$@" && echo "True" || echo "False";
}
```
