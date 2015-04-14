title: "Android content command"
date: 2015-01-13 13:02:49
categories:
- android
tags:
- shell-tool
- content
- settings
toc: true
---

Notes for interacting with ContentProvider in console on Android system.

<!-- more -->

## `content` command

```
usage: adb shell content [subcommand] [options]

usage: adb shell content insert --uri <URI> [--user <USER_ID>] --bind <BINDING> [--bind <BINDING>...]
  <URI> a content provider URI.
  <BINDING> binds a typed value to a column and is formatted:
  <COLUMN_NAME>:<TYPE>:<COLUMN_VALUE> where:
  <TYPE> specifies data type such as:
  b - boolean, s - string, i - integer, l - long, f - float, d - double
  Note: Omit the value for passing an empty string, e.g column:s:
  Example:
  # Add "new_setting" secure setting with value "new_value".
  adb shell content insert --uri content://settings/secure --bind name:s:new_setting --bind value:s:new_value

usage: adb shell content update --uri <URI> [--user <USER_ID>] [--where <WHERE>]
  <WHERE> is a SQL style where clause in quotes (You have to escape single quotes - see example below).
  Example:
  # Change "new_setting" secure setting to "newer_value".
  adb shell content update --uri content://settings/secure --bind value:s:newer_value --where "name=\'new_setting\'"

usage: adb shell content delete --uri <URI> [--user <USER_ID>] --bind <BINDING> [--bind <BINDING>...] [--where <WHERE>]
  Example:
  # Remove "new_setting" secure setting.
  adb shell content delete --uri content://settings/secure --where "name=\'new_setting\'"

usage: adb shell content query --uri <URI> [--user <USER_ID>] [--projection <PROJECTION>] [--where <WHERE>] [--sort <SORT_ORDER>]
  <PROJECTION> is a list of colon separated column names and is formatted:
  <COLUMN_NAME>[:<COLUMN_NAME>...]
  <SORT_OREDER> is the order in which rows in the result should be sorted.
  Example:
  # Select "name" and "value" columns from secure settings where "name" is equal to "new_setting" and sort the result by name in ascending order.
  adb shell content query --uri content://settings/secure --projection name:value --where "name=\'new_setting\'" --sort "name ASC"
```

## pulling database from device

```sh
# pull databases/
cd /data/data; busybox find . -type d -name databases -type d | busybox xargs busybox tar cf /sdcard/databases.tar
adbpull databases.tar
tar xf databases.tar
```

```sh
# pull data/data
cd /data/data; busybox tar cf /sdcard/data.tar .
adbpull data.tar
tar xf data.tar
```

## `settings` command

```
usage:  settings [--user NUM] get namespace key
        settings [--user NUM] put namespace key value

'namespace' is one of {system, secure, global}, case-insensitive
If '--user NUM' is not given, the operations are performed on the owner user.
```

## samples

### Settings

Settings database located at `/data/data/com.android.providers.settings/databases/settings.db`

```sh
content query --uri content://settings/secure
# this fails, better to use settings
content update --uri content://com.google.settings/partner --bind value:s:gps --where name="\'location_providers_allowed\'"

settings get system screen_off_timeout
settings put system screen_off_timeout 36000000
# use `content query` to list keys in `{system, secure, global}` table
```

### `com.google.settings/partner`

```sh
content query --uri content://com.google.settings/partner
content update --uri content://com.google.settings/partner --bind value:i:0 --where name="\'network_location_opt_in\'"
```
