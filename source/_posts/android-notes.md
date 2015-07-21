title: "Android notes"
date: 2014-12-17 13:45:27
categories:
- android
tags:
- adb
- aapt
- wakelock
- input
- logcat
- notes
toc: true
---

Notes for console tools available on Android system.

[Android (and Friends) Reading Guide | Linux.org](http://www.linux.org/threads/android-and-friends-reading-guide.6146/)
[hellogv的专栏 - 博客频道 - CSDN.NET](http://blog.csdn.net/hellogv)

## Dev

[AndroidXRef](http://androidxref.com/)
[Detect and Resolve Performance Problems on Android - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/detect-and-resolve-performance-problems-on-android--cms-24058)

> attach adbpull, adbpush, adbview, adbcmd here

<!-- more -->

* prettify /proc/wakelocks

  ```sh
  # on device
  cat /proc/wakelocks | busybox awk '{ printf "%-25s %-10s\n", $1, $5 }' | busybox grep -v " 0"

  # with adb
  adb shell cat /proc/wakelocks | awk '{ printf "%-25s %-10s\n", $1, $5 }' | grep -v " 0"
  ```

* input device info

  ```sh
  cat /proc/bus/input/devices
  ```

## adb

http://developer.android.com/tools/help/adb.html

`adb` comes with the Android SDK.
Windows user can use the package [here](http://forum.xda-developers.com/showthread.php?t=2588979).

### Enable adb via TCP

On PC:
```sh
adb tcpip 5555
```

On device (need ROOT):
```sh
su
setprop service.adb.tcp.port 5555
stop adbd
start adbd
```

```sh
adb connect <DEVICE_IP_ADDRESS>:5555
```

## Remote mouse

[悟空遥控器](https://play.google.com/store/apps/details?id=com.wukongtv.wkremote.client) is an Android app that is able to allow mobile to control Android STB remotely. The server app does not require rooting and system integration. It draws the cursor on an overlay layer and issue commands to `Input` framework.

[Programmatically Injecting Events on Android - Part 1 - PocketMagic](http://www.pocketmagic.net/injecting-events-programatically-on-android/)
[Programmatically Injecting Events on Android - Part 2 - PocketMagic](http://www.pocketmagic.net/programmatically-injecting-events-on-android-part-2/)
[Android Overlay Mouse Cursor - PocketMagic](http://www.pocketmagic.net/android-overlay-cursor/)

## logcat

### logcat filtering (Eclipse and Android Studio)

pid:
text:
app: package name (`com.example.android.bluetoothlegatt`)
tag: `^(?!.*(DeskClock|dalvik|wpa)).*$`, `^(?!(BluetoothAdapter|AbsListView))`

### android-log-viewer

https://bitbucket.org/mlopatkin/android-log-viewer

### logcat (node)

https://www.npmjs.com/package/logcat

### pidcat (python)

https://github.com/JakeWharton/pidcat

## Android on Chrome

[Android Apps on Linux | Linux.org](http://www.linux.org/threads/android-apps-on-linux.7431/)

## aapt

```
Android Asset Packaging Tool

Usage:
 aapt l[ist] [-v] [-a] file.{zip,jar,apk}
   List contents of Zip-compatible archive.

 aapt d[ump] [--values] [--include-meta-data] WHAT file.{apk} [asset [asset ...]]
   strings          Print the contents of the resource table string pool in the APK.
   badging          Print the label and icon for the app declared in APK.
   permissions      Print the permissions from the APK.
   resources        Print the resource table from the APK.
   configurations   Print the configurations in the APK.
   xmltree          Print the compiled xmls in the given assets.
   xmlstrings       Print the strings of the given compiled xml assets.

 aapt p[ackage] [-d][-f][-m][-u][-v][-x][-z][-M AndroidManifest.xml] \
        [-0 extension [-0 extension ...]] [-g tolerance] [-j jarfile] \
        [--debug-mode] [--min-sdk-version VAL] [--target-sdk-version VAL] \
        [--app-version VAL] [--app-version-name TEXT] [--custom-package VAL] \
        [--rename-manifest-package PACKAGE] \
        [--rename-instrumentation-target-package PACKAGE] \
        [--utf16] [--auto-add-overlay] \
        [--max-res-version VAL] \
        [-I base-package [-I base-package ...]] \
        [-A asset-source-dir]  [-G class-list-file] [-P public-definitions-file] \
        [-S resource-sources [-S resource-sources ...]] \
        [-F apk-file] [-J R-file-dir] \
        [--product product1,product2,...] \
        [-c CONFIGS] [--preferred-configurations CONFIGS] \
        [--split CONFIGS [--split CONFIGS]] \
        [--feature-of package [--feature-after package]] \
        [raw-files-dir [raw-files-dir] ...] \
        [--output-text-symbols DIR]

   Package the android resources.  It will read assets and resources that are
   supplied with the -M -A -S or raw-files-dir arguments.  The -J -P -F and -R
   options control which files are output.

 aapt r[emove] [-v] file.{zip,jar,apk} file1 [file2 ...]
   Delete specified files from Zip-compatible archive.

 aapt a[dd] [-v] file.{zip,jar,apk} file1 [file2 ...]
   Add specified files to Zip-compatible archive.

 aapt c[runch] [-v] -S resource-sources ... -C output-folder ...
   Do PNG preprocessing on one or several resource folders
   and store the results in the output folder.

 aapt s[ingleCrunch] [-v] -i input-file -o outputfile
   Do PNG preprocessing on a single file.

 aapt v[ersion]
   Print program version.

 Modifiers:
   -a  print Android-specific data (resources, manifest) when listing
   -c  specify which configurations to include.  The default is all
       configurations.  The value of the parameter should be a comma
       separated list of configuration values.  Locales should be specified
       as either a language or language-region pair.  Some examples:
            en
            port,en
            port,land,en_US
   -d  one or more device assets to include, separated by commas
   -f  force overwrite of existing files
   -g  specify a pixel tolerance to force images to grayscale, default 0
   -j  specify a jar or zip file containing classes to include
   -k  junk path of file(s) added
   -m  make package directories under location specified by -J
       comes before this one. The first Feature Split APK should not define
       anything here.
   --rename-manifest-package
       Rewrite the manifest so that its package name is the package name
       given here.  Relative class names (for example .Foo) will be
       changed to absolute names with the old package so that the code
       does not need to change.
   --rename-instrumentation-target-package
       Rewrite the manifest so that all of its instrumentation
       components target the given package.  Useful when used in
       conjunction with --rename-manifest-package to fix tests against
       a package that has been renamed.
   --product
       Specifies which variant to choose for strings that have
       product variants
   --utf16
       changes default encoding for resources to UTF-16.  Only useful when API
       level is set to 7 or higher where the default encoding is UTF-8.
   --non-constant-id
       Make the resources ID non constant. This is required to make an R java class
       that does not contain the final value but is used to make reusable compiled
       libraries that need to access resources.
   --shared-lib
       Make a shared library resource package that can be loaded by an application
       at runtime to access the libraries resources. Implies --non-constant-id.
   --error-on-failed-insert
       Forces aapt to return an error if it fails to insert values into the manifest
       with --debug-mode, --min-sdk-version, --target-sdk-version --version-code
       and --version-name.
       Insertion typically fails if the manifest already defines the attribute.
   --error-on-missing-config-entry
       Forces aapt to return an error if it fails to find an entry for a configuration.
   --output-text-symbols
       Generates a text file containing the resource symbols of the R class in the
       specified folder.
   --ignore-assets
       Assets to be ignored. Default pattern is:
       !.svn:!.git:!.ds_store:!*.scc:.*:<dir>_*:!CVS:!thumbs.db:!picasa.ini:!*~
```
