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

[tokozedg/sman: Command-line snippet manager](https://github.com/tokozedg/sman)

## Watch files

### `inotifywait`

[Home · rvoicilas/inotify-tools Wiki](https://github.com/rvoicilas/inotify-tools/wiki)
[linux - How to execute a command whenever a file changes? - Super User](https://superuser.com/a/181543/82502)

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

### watchman

[Watchman A file watching service | Watchman](https://facebook.github.io/watchman/)

seems complicated on Windows

### watchr

[bevry/watchr: Better file system watching for Node.js. Provides a normalised API the file watching APIs of different node versions, nested/recursive file and directory watching, and accurate detailed events for file/directory changes, deletions and creations.](https://github.com/bevry/watchr)

### chokidar

[paulmillr/chokidar: A neat wrapper around node.js fs.watch / fs.watchFile / FSEvents](https://github.com/paulmillr/chokidar)

[kimmobrunfeldt/chokidar-cli: Fast cross-platform cli utility to watch file system changes](https://github.com/kimmobrunfeldt/chokidar-cli)

### gaze

[shama/gaze: A globbing fs.watch wrapper built from the best parts of other fine watch libs.](https://github.com/shama/gaze)

[doowb/watch-cli: Watch files and execute an npm script when files change.](https://github.com/doowb/watch-cli)

## loop files

```sh
while IFS= read -r -d '' file; do
  some command "$file"
done < <(find . -type f -name '*.csv' -print0)
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
