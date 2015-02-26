title: Android notes
toc: true
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
---

> attach adbpull, adbpush, adbview, adbcmd here

<!-- more -->

* prettify /proc/wakelocks

  ```sh
  cat /proc/wakelocks | busybox awk '{ printf "%-25s %-10s\n", $1, $5 }' | busybox grep -v " 0"

  adb shell cat /proc/wakelocks | awk '{ printf "%-25s %-10s\n", $1, $5 }' | grep -v " 0"
  ```

* input device info

  ```sh
  cat /proc/bus/input/devices
  ```

* pulling database from device

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

## aapt

```
Android Asset Packaging Tool

Usage:
 aapt l[ist] [-v] [-a] file.{zip,jar,apk}
   List contents of Zip-compatible archive.

 aapt d[ump] [--values] WHAT file.{apk} [asset [asset ...]]
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
       If you put the special locale, zz_ZZ on the list, it will perform
       pseudolocalization on the default locale, modifying all of the
       strings so you can look for strings that missed the
       internationalization process.  For example:
            port,land,zz_ZZ
   -d  one or more device assets to include, separated by commas
   -f  force overwrite of existing files
   -g  specify a pixel tolerance to force images to grayscale, default 0
   -j  specify a jar or zip file containing classes to include
   -k  junk path of file(s) added
   -m  make package directories under location specified by -J
   -u  update existing packages (add new, replace older, remove deleted files)
   -v  verbose output
   -x  create extending (non-application) resource IDs
   -z  require localization of resource attributes marked with
       localization="suggested"
   -A  additional directory in which to find raw asset files
   -G  A file to output proguard options into.
   -F  specify the apk file to output
   -I  add an existing package to base include set
   -J  specify where to output R.java resource constant definitions
   -M  specify full path to AndroidManifest.xml to include in zip
   -P  specify where to output public resource definitions
   -S  directory in which to find resources.  Multiple directories will be scanned
       and the first match found (left to right) will take precedence.
   -0  specifies an additional extension for which such files will not
       be stored compressed in the .apk.  An empty string means to not
       compress any files at all.
   --debug-mode
       inserts android:debuggable="true" in to the application node of the
       manifest, making the application debuggable even on production devices.
   --min-sdk-version
       inserts android:minSdkVersion in to manifest.  If the version is 7 or
       higher, the default encoding for resources will be in UTF-8.
   --target-sdk-version
       inserts android:targetSdkVersion in to manifest.
   --max-res-version
       ignores versioned resource directories above the given value.
   --values
       when used with "dump resources" also includes resource values.
   --version-code
       inserts android:versionCode in to manifest.
   --version-name
       inserts android:versionName in to manifest.
   --custom-package
       generates R.java into a different package.
   --extra-packages
       generate R.java for libraries. Separate libraries with ':'.
   --generate-dependencies
       generate dependency files in the same directories for R.java and resource package
   --auto-add-overlay
       Automatically add resources that are only in overlays.
   --preferred-configurations
       Like the -c option for filtering out unneeded configurations, but
       only expresses a preference.  If there is no resource available with
       the preferred configuration then it will not be stripped.
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
   --error-on-failed-insert
       Forces aapt to return an error if it fails to insert values into the manifest
       with --debug-mode, --min-sdk-version, --target-sdk-version --version-code
       and --version-name.
       Insertion typically fails if the manifest already defines the attribute.
   --output-text-symbols
       Generates a text file containing the resource symbols of the R class in the
       specified folder.
   --ignore-assets
       Assets to be ignored. Default pattern is:
       !.svn:!.git:!.ds_store:!*.scc:.*:<dir>_*:!CVS:!thumbs.db:!picasa.ini:!*~
```

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
