---
title: nVidia Jetson
categories:
  - maker
tags:
  - iot
  - jetson
toc: true
date: 2019-08-09 12:13:12
---

[Nvidia Jetson - Wikiwand](https://www.wikiwand.com/en/Nvidia_Jetson)

[Embedded AI Modules: NVIDIA's Jetson TX2, Nano & AGX Xavier | Arrow.com](https://www.arrow.com/en/research-and-events/articles/comparing-embedded-ai-modules-nvidias-jetson-nano-tx2--and-agx-xavier)

## Jetson Nano

[NVIDIA Jetson Nano Developer Kit | NVIDIA Developer](https://developer.nvidia.com/embedded/jetson-nano-developer-kit)
[The Power of Modern AI to Millions of Devices | NVIDIA Jetson Nano](https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/jetson-nano/)
[Jetson Nano - eLinux.org](https://elinux.org/Jetson_Nano)

[NVIDIA Jetson Nano .img pre-configured for Deep Learning and Computer Vision - PyImageSearch](https://www.pyimagesearch.com/2020/03/04/nvidia-jetson-nano-img-pre-configured-for-deep-learning-and-computer-vision/)
[How to configure your NVIDIA Jetson Nano for Computer Vision and Deep Learning - PyImageSearch](https://www.pyimagesearch.com/2020/03/25/how-to-configure-your-nvidia-jetson-nano-for-computer-vision-and-deep-learning/)

## Jetson TX2

[High Performance AI at the Edge | NVIDIA Jetson TX2](https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/jetson-tx2/)
[Harness AI at the Edge with the Jetson TX2 Developer Kit | NVIDIA Developer](https://developer.nvidia.com/embedded/jetson-tx2-developer-kit)
[NVIDIA Announces Jetson TX2: Parker Comes To NVIDIA’s Embedded System Kit - Print View](https://www.anandtech.com/print/11185/nvidia-announces-jetson-tx2-parker)
[Jetson TX2 - eLinux.org](https://elinux.org/Jetson_TX2)

## Jetson Xavier

[World’s Smallest AI Supercomputer: Jetson Xavier NX | NVIDIA](https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/jetson-xavier-nx/)
[Jetson Xavier NX | NVIDIA Developer](https://developer.nvidia.com/embedded/jetson-xavier-nx)
[NVIDIA Gives Jetson AGX Xavier a Trim, Announces Nano-Sized Jetson Xavier NX - Print View](https://www.anandtech.com/print/15070/nvidia-gives-jetson-xavier-a-trim-announces-nanosized-jetson-xavier-nx)
[NVIDIA 推出 Jetson Xavier NX 輕量 AI 電腦，效能較 Jetson Nano 提升 4 倍 | T 客邦](https://www.techbang.com/posts/74096-nvidia-launches-jetson-xavier-nx-lightweight-ai-computer-four-times-more-powerful-than-jetson-nano)

---

## Cross Compile Qt5

There are two major steps:

- build `Qt` for a given `nVidia Jetson TX2` device on Linux host.
- build the `Qt` application using the above compiled `Qt` libs.

1. `Jetson TX2` os image.

   [NVIDIA JetPack Software](https://developer.nvidia.com/embedded/develop/software)

   ```sh
   frankchen@:jetson-tx2$ ll /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/
   total 96
   drwxr-xr-x  21 root      root       4096 Jun 18 16:36 ./
   drwxr-xr-x   6 frankchen frankchen  4096 Mar 13 15:40 ../
   drwxr-xr-x   2 root      root       4096 Feb 20 15:22 bin/
   drwxr-xr-x   3 root      root       4096 Jun 18 16:37 boot/
   drwxr-xr-x   2 root      root       4096 May 18  2018 dev/
   drwxr-xr-x 135 root      root      12288 Jun 18 16:37 etc/
   drwxr-xr-x   2 root      root       4096 Apr 24  2018 home/
   drwxr-xr-x  21 root      root       4096 Jun 18 16:37 lib/
   drwxr-xr-x   2 root      root       4096 Aug  6  2018 media/
   drwxr-xr-x   2 root      root       4096 Apr 27  2018 mnt/
   drwxr-xr-x   3 root      root       4096 Jun 18 16:37 opt/
   drwxr-xr-x   2 root      root       4096 Apr 24  2018 proc/
   -rw-r--r--   1 frankchen frankchen    62 Mar 13 15:40 README.txt
   drwx------   2 root      root       4096 Apr 27  2018 root/
   drwxr-xr-x  16 root      root       4096 Jan  4 09:20 run/
   drwxr-xr-x   2 root      root       4096 Feb 20 15:22 sbin/
   drwxr-xr-x   2 root      root       4096 May 11  2018 snap/
   drwxr-xr-x   2 root      root       4096 Apr 27  2018 srv/
   drwxr-xr-x   2 root      root       4096 Apr 24  2018 sys/
   drwxrwxrwt   2 root      root       4096 Feb 21 19:52 tmp/
   drwxr-xr-x  11 root      root       4096 May 21  2018 usr/
   drwxr-xr-x  15 root      root       4096 Jun 18 16:37 var/

   ```

2. toolchains for `Jetson TX2` on linux.

   go to [Linaro Download Center](https://releases.linaro.org/components/toolchain/binaries/5.5-2017.10/aarch64-linux-gnu/), find product with title `5.5.0-2017.10-x86_64_arrch64`.

   ```sh
   frankchen@:jetson-tx2$ tar -xvf ~/Downloads/gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu.tar.xz
   frankchen@:jetson-tx2$ mv gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/ toolchains/
   frankchen@:jetson-tx2$ ll toolchains/
   total 16
   drwxr-xr-x 4 frankchen frankchen 4096 Jun 20 17:13 ./
   drwxr-xr-x 4 frankchen frankchen 4096 Jun 20 17:01 ../
   drwxr-xr-x 8 frankchen frankchen 4096 Jan 28  2017 gcc-linaro-5.4.1-2017.01-x86_64_aarch64-linux-gnu/
   drwxr-xr-x 8 frankchen frankchen 4096 Jan 23 04:22 gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu/

   ```

   symbolic link tool,

   ```sh
   frankchen@:jetson-tx2$ wget https://raw.githubusercontent.com/riscv/riscv-poky/master/scripts/sysroot-relativelinks.py
   frankchen@:jetson-tx2$ chmod +x ./sysroot-relativelinks.py
   frankchen@:jetson-tx2$ sudo ./sysroot-relativelinks.py $TX2_SYSROOT
   ```

   **Note:**

   ```sh
   # Ubuntu 18.04, the toolchain maybe have errors below
   frankchen@:jetson-tx2$ ./toolchains/bin/aarch64-unknown-linux-gnu-gcc
   aarch64-unknown-linux-gnu-gcc: loadlocale.c:129: _nl_intern_locale_data: Assertion ''cnt < (sizeof (_nl_value_type_LC_TIME) / sizeof (_nl_value_type_LC_TIME[0]))'' failed.
   Aborted (core dumped)
   # Fix
   frankchen@:jetson-tx2$ export LC_ALL=C
   frankchen@:jetson-tx2$ ./toolchains/bin/aarch64-unknown-linux-gnu-gcc
   aarch64-unknown-linux-gnu-gcc: fatal error: no input files
   compilation terminated.
   # Sysroot for the toolchain
   frankchen@:jetson-tx2$ ./toolchains/bin/aarch64-unknown-linux-gnu-gcc --print-sysroot
   /home/frankchen/Documents/jetson-tx2/toolchains/bin/../aarch64-unknown-linux-gnu/sysroot

   ```

3. configure to build `Qt` for `nvidia Jetson TX2` on linux host

   ```sh
   # cd <QT_SRC>
   frankchen@:jetson-tx2$ cd ~/Qt/5.12.3/Src/

   # set ENV
   frankchen@:jetson-tx2$ export TX2_SYSROOT=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs
   frankchen@:jetson-tx2$ export TX2_TOOLCHAIN=/home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-

   # configure
   frankchen@:Src$ ./configure -opensource -confirm-license \
       -release \
       -device linux-jetson-tx2-g++ \
       -device-option CROSS_COMPILE=$TX2_TOOLCHAIN \
       -sysroot $TX2_SYSROOT \
       -extprefix ~/Documents/jetson-tx2/qt5-jetson-tx2 \
       -nomake tests -nomake examples \
       -skip qtwayland -skip qtlocation -skip qtscript

   ```

   **Note:**

   > -prefix, -extprefix, and -hostprefix control the intended destination directory of the Qt build. In the above example the ARM build of Qt is expected to be placed in /usr/local/qt5 on the target device. Note that running make install does not deploy anything to the device. Instead, the install step targets the directory specified by extprefix which defaults to sysroot + prefix and is therefore optional. However, in many cases "polluting" the sysroot is not desirable and thus specifying -extprefix becomes important. Finally, -hostprefix allows separating host tools like qmake, rcc, uic from the binaries for the target. When given, such tools will be installed under the specified directory instead of extprefix.

4. make build

   ```sh
   frankchen@:Src$ make clean
   frankchen@:Src$ make -j4
   frankchen@:Src$ make install
   # the Qt libs will be installed into  `extprefix` folder
   frankchen@:Src$ ll ~/Documents/jetson-tx2/qt5-jetson-tx2/
   total 64
   drwxr-xr-x 10 frankchen frankchen  4096 Jun 20 19:20 ./
   drwxr-xr-x  4 frankchen frankchen  4096 Jun 20 17:01 ../
   drwxr-xr-x  2 frankchen frankchen  4096 Jun 20 19:20 bin/
   drwxr-xr-x  3 frankchen frankchen  4096 Jun 20 14:11 doc/
   drwxr-xr-x 76 frankchen frankchen  4096 Jun 20 19:20 include/
   drwxr-xr-x  4 frankchen frankchen 20480 Jun 20 19:20 lib/
   drwxr-xr-x 79 frankchen frankchen  4096 Jun 20 19:19 mkspecs/
   drwxr-xr-x 22 frankchen frankchen  4096 Jun 20 19:20 plugins/
   drwxr-xr-x 23 frankchen frankchen  4096 Jun 20 19:20 qml/
   drwxr-xr-x  2 frankchen frankchen 12288 Jun 20 19:20 translations/
   ```

   **Problems:**

   1. errors when building `libwebp`,

   ```sh
   frankchen@:Src$ make
   make[5]: Entering directory '/home/frankchen/Qt/5.12.3/Src/qtimageformats/src/plugins/imageformats/webp'
   /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.4.1-2017.01-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-gcc -c -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O2 -std=gnu11 -fvisibility=hidden -fno-exceptions -Wall -W -D_REENTRANT -fPIC -DQT_DEPRECATED_WARNINGS -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_NO_EXCEPTIONS -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I. -I../../../3rdparty/libwebp -I../../../3rdparty/libwebp/src -I../../../3rdparty/libwebp/src/dec -I../../../3rdparty/libwebp/src/enc -I../../../3rdparty/libwebp/src/dsp -I../../../3rdparty/libwebp/src/mux -I../../../3rdparty/libwebp/src/utils -I../../../3rdparty/libwebp/src/webp -I/home/frankchen/Qt/5.12.3/Src/qtbase/include -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtGui -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtCore -I.moc -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/libdrm -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I/home/frankchen/Qt/5.12.3/Src/qtbase/mkspecs/devices/linux-jetson-tx2-g++ -o .obj/dec_neon.o ../../../3rdparty/libwebp/src/dsp/dec_neon.c
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c: In function 'SimpleHFilter16_NEON':
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c:531:1: internal compiler error: in record_operand_use, at regrename.c:220
   }
   ^

   # enter into the folder to better tackle this issue
   frankchen@:Src$ cd /home/frankchen/Qt/5.12.3/Src/qtimageformats/src/plugins/imageformats/webp
   frankchen@:webp$ make clean
   frankchen@:webp$ /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.4.1-2017.01-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-gcc -c -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O2 -std=gnu11 -fvisibility=hidden -fno-exceptions -Wall -W -D_REENTRANT -fPIC -DQT_DEPRECATED_WARNINGS -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_NO_EXCEPTIONS -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I. -I../../../3rdparty/libwebp -I../../../3rdparty/libwebp/src -I../../../3rdparty/libwebp/src/dec -I../../../3rdparty/libwebp/src/enc -I../../../3rdparty/libwebp/src/dsp -I../../../3rdparty/libwebp/src/mux -I../../../3rdparty/libwebp/src/utils -I../../../3rdparty/libwebp/src/webp -I/home/frankchen/Qt/5.12.3/Src/qtbase/include -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtGui -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtCore -I.moc -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/libdrm -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I/home/frankchen/Qt/5.12.3/Src/qtbase/mkspecs/devices/linux-jetson-tx2-g++ -o .obj/dec_neon.o ../../../3rdparty/libwebp/src/dsp/dec_neon.c
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c: In function 'SimpleHFilter16_NEON':
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c:531:1: internal compiler error: in record_operand_use, at regrename.c:220
   }
   ^
   Please submit a full bug report,
   with preprocessed source if appropriate.
   See <http://gcc.gnu.org/bugs.html> for instructions.


   # possible solution, using the linaro toolchain with new version(5.5.0-2017.10) maybe fix the bug
   frankchen@:webp$ make clean
   frankchen@:webp$ /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-gcc -c -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O2 -std=gnu11 -fvisibility=hidden -fno-exceptions -Wall -W -D_REENTRANT -fPIC -DQT_DEPRECATED_WARNINGS -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_NO_EXCEPTIONS -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I. -I../../../3rdparty/libwebp -I../../../3rdparty/libwebp/src -I../../../3rdparty/libwebp/src/dec -I../../../3rdparty/libwebp/src/enc -I../../../3rdparty/libwebp/src/dsp -I../../../3rdparty/libwebp/src/mux -I../../../3rdparty/libwebp/src/utils -I../../../3rdparty/libwebp/src/webp -I/home/frankchen/Qt/5.12.3/Src/qtbase/include -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtGui -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtCore -I.moc -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/libdrm -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I/home/frankchen/Qt/5.12.3/Src/qtbase/mkspecs/devices/linux-jetson-tx2-g++ -o .obj/dec_neon.o ../../../3rdparty/libwebp/src/dsp/dec_neon.c

   ```

   similar problems found online:

   - (Internal compiler error using -mtune=cortex-a57.cortex-a53 with linaro gcc 5.2.1)[https://bugs.linaro.org/show_bug.cgi?id=2785]
   - (Errors buliding libwebp on NVIDIA TX2 with Linaro gcc-5.4.0 using flags)[https://github.com/opencv/opencv/issues/12322]
   - (internal compiler error in record_operand_use)[https://www.mail-archive.com/gcc-bugs@gcc.gnu.org/msg472065.html]

   1. stdlib.h

   ```sh
   make[3]: Entering directory '/home/frankchen/Qt/5.12.3/Src/qtbase/src/corelib'
   /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-g++ -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O3 -std=c++1y -fvisibility=hidden -fvisibility-inlines-hidden -Wall -W -Wvla -Wdate-time -D_REENTRANT -fPIC -DQT_NO_USING_NAMESPACE -DQT_NO_FOREACH -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_BUILD_CORE_LIB -DQT_BUILDING_QT -DQT_NO_CAST_TO_ASCII -DQT_ASCII_CAST_WARNINGS -DQT_MOC_COMPAT -DQT_USE_QSTRINGBUILDER -DQT_DEPRECATED_WARNINGS -DQT_DISABLE_DEPRECATED_BEFORE=0x050000 -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DPCRE2_CODE_UNIT_WIDTH=16 -I. -Iglobal -I../3rdparty/harfbuzz/src -I../3rdparty/md5 -I../3rdparty/md4 -I../3rdparty/sha3 -I../3rdparty -I../3rdparty/double-conversion/include -I../3rdparty/double-conversion/include/double-conversion -I../3rdparty/forkfd -I../3rdparty/tinycbor/src -I../../include -I../../include/QtCore -I../../include/QtCore/5.12.3 -I../../include/QtCore/5.12.3/QtCore -I.moc -I.tracegen -I../3rdparty/pcre2/src -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/glib-2.0 -I/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/lib/aarch64-linux-gnu/glib-2.0/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I../../mkspecs/devices/linux-jetson-tx2-g++ -x c++-header -c global/qt_pch.h -o .pch/Qt5Core.gch/c++
   In file included from /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/aarch64-linux-gnu/include/c++/7.4.1/bits/stl_algo.h:59:0,
                   from /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/aarch64-linux-gnu/include/c++/7.4.1/algorithm:62,
                   from global/qglobal.h:142,
                   from global/qt_pch.h:56:
   /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/aarch64-linux-gnu/include/c++/7.4.1/cstdlib:75:15: fatal error: stdlib.h: No such file or directory
   #include_next <stdlib.h>
               ^~~~~~~~~~
   # possible solution, using the linaro toolchain with new version(5.5.0-2017.10) maybe fix the bug
   ```

5. build a `Qt` application for `Jetson TX2` on linux host

   ```sh
   # cd <Project folder>
   frankchen@:build-TextFinder-JetsonTx2$ cd ~/Documents/qt-project/
   frankchen@:qt-project$ ll
   total 32
   drwxr-xr-x  8 frankchen frankchen 4096 Jun 21 11:00 ./
   drwxrwxrwx 26 frankchen frankchen 4096 Jun 18 17:11 ../
   drwxrwxr-x  2 frankchen frankchen 4096 Jun 13 15:12 build-TextFinder-Android_for_arm64_v8a_Clang_Qt_5_12_3_for_Android_ARM64_v8a-Release/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 12 12:50 build-TextFinder-Desktop_Qt_5_12_3_GCC_64bit-Release/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 12 16:26 build-TextFinder-Desktop_Qt_5_12_3_Win/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 21 11:03 build-TextFinder-JetsonTx2/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 17 16:39 build-TextFinder-RaspberryPi/
   drwxrwxr-x  2 frankchen frankchen 4096 Jun 13 15:12 TextFinder/

   # create build folder and cd into
   frankchen@:qt-project$ mkdir build-TextFinder-JetsonTx2
   frankchen@:qt-project$ cd build-TextFinder-JetsonTx2/

   # create `Makefile` using `qmake` tool
   frankchen@:build-TextFinder-JetsonTx2$ "/home/frankchen/Documents/jetson-tx2/qt5-jetson-tx2/bin/qmake" /home/frankchen/Documents/qt-project/TextFinder/TextFinder.pro

   # build executable file
   frankchen@:build-TextFinder-JetsonTx2$ make -j4
   frankchen@:build-TextFinder-JetsonTx2$ file TextFinder
   TextFinder: ELF 64-bit LSB executable, ARM aarch64, version 1 (SYSV), dynamically linked, interpreter /lib/ld-, for GNU/Linux 3.7.0, BuildID[sha1]=248f556bb9b9dfa0329b54b918f919ce406da67b, not stripped
   ```

**References:**

- [NVIDIA JetPack Software](https://developer.nvidia.com/embedded/develop/software)
- [CUDA Development for Jetson with NVIDIA Nsight Eclipse Edition](https://devblogs.nvidia.com/cuda-jetson-nvidia-nsight-eclipse-edition/)

### Compile Qt program for `nVidia Jetson TX2` on Linux host(advanced example)

There are two major steps:

- build `Qt` for a given `nVidia Jetson TX2` device on Linux host.
- build the `Qt` application using the above compiled `Qt` libs.

1. `Jetson TX2` os image.

   [NVIDIA JetPack Software](https://developer.nvidia.com/embedded/develop/software)

   ```sh
   frankchen@:jetson-tx2$ ll /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/
   total 96
   drwxr-xr-x  21 root      root       4096 Jun 18 16:36 ./
   drwxr-xr-x   6 frankchen frankchen  4096 Mar 13 15:40 ../
   drwxr-xr-x   2 root      root       4096 Feb 20 15:22 bin/
   drwxr-xr-x   3 root      root       4096 Jun 18 16:37 boot/
   drwxr-xr-x   2 root      root       4096 May 18  2018 dev/
   drwxr-xr-x 135 root      root      12288 Jun 18 16:37 etc/
   drwxr-xr-x   2 root      root       4096 Apr 24  2018 home/
   drwxr-xr-x  21 root      root       4096 Jun 18 16:37 lib/
   drwxr-xr-x   2 root      root       4096 Aug  6  2018 media/
   drwxr-xr-x   2 root      root       4096 Apr 27  2018 mnt/
   drwxr-xr-x   3 root      root       4096 Jun 18 16:37 opt/
   drwxr-xr-x   2 root      root       4096 Apr 24  2018 proc/
   -rw-r--r--   1 frankchen frankchen    62 Mar 13 15:40 README.txt
   drwx------   2 root      root       4096 Apr 27  2018 root/
   drwxr-xr-x  16 root      root       4096 Jan  4 09:20 run/
   drwxr-xr-x   2 root      root       4096 Feb 20 15:22 sbin/
   drwxr-xr-x   2 root      root       4096 May 11  2018 snap/
   drwxr-xr-x   2 root      root       4096 Apr 27  2018 srv/
   drwxr-xr-x   2 root      root       4096 Apr 24  2018 sys/
   drwxrwxrwt   2 root      root       4096 Feb 21 19:52 tmp/
   drwxr-xr-x  11 root      root       4096 May 21  2018 usr/
   drwxr-xr-x  15 root      root       4096 Jun 18 16:37 var/
   ```

2. toolchains for `Jetson TX2` on linux.

   go to [Linaro Download Center](https://releases.linaro.org/components/toolchain/binaries/5.5-2017.10/aarch64-linux-gnu/), find product with title `5.5.0-2017.10-x86_64_arrch64`.

   ```sh
   frankchen@:jetson-tx2$ tar -xvf ~/Downloads/gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu.tar.xz
   frankchen@:jetson-tx2$ mv gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/ toolchains/
   frankchen@:jetson-tx2$ ll toolchains/
   total 16
   drwxr-xr-x 4 frankchen frankchen 4096 Jun 20 17:13 ./
   drwxr-xr-x 4 frankchen frankchen 4096 Jun 20 17:01 ../
   drwxr-xr-x 8 frankchen frankchen 4096 Jan 28  2017 gcc-linaro-5.4.1-2017.01-x86_64_aarch64-linux-gnu/
   drwxr-xr-x 8 frankchen frankchen 4096 Jan 23 04:22 gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu/
   ```

   symbolic link tool,

   ```sh
   frankchen@:jetson-tx2$ wget https://raw.githubusercontent.com/riscv/riscv-poky/master/scripts/sysroot-relativelinks.py
   frankchen@:jetson-tx2$ chmod +x ./sysroot-relativelinks.py
   frankchen@:jetson-tx2$ sudo ./sysroot-relativelinks.py $TX2_SYSROOT
   ```

   **Note:**

   ```sh
   # Ubuntu 18.04, the toolchain maybe have errors below
   frankchen@:jetson-tx2$ ./toolchains/bin/aarch64-unknown-linux-gnu-gcc
   aarch64-unknown-linux-gnu-gcc: loadlocale.c:129: _nl_intern_locale_data: Assertion ''cnt < (sizeof (_nl_value_type_LC_TIME) / sizeof (_nl_value_type_LC_TIME[0]))'' failed.
   Aborted (core dumped)
   # Fix
   frankchen@:jetson-tx2$ export LC_ALL=C
   frankchen@:jetson-tx2$ ./toolchains/bin/aarch64-unknown-linux-gnu-gcc
   aarch64-unknown-linux-gnu-gcc: fatal error: no input files
   compilation terminated.
   # Sysroot for the toolchain
   frankchen@:jetson-tx2$ ./toolchains/bin/aarch64-unknown-linux-gnu-gcc --print-sysroot
   /home/frankchen/Documents/jetson-tx2/toolchains/bin/../aarch64-unknown-linux-gnu/sysroot
   ```

3. configure to build `Qt` for `nvidia Jetson TX2` on linux host

   ```sh
   # cd <QT_SRC>
   frankchen@:jetson-tx2$ cd ~/Qt/5.12.3/Src/

   # set ENV
   frankchen@:jetson-tx2$ export TX2_SYSROOT=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs
   frankchen@:jetson-tx2$ export TX2_TOOLCHAIN=/home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-

   # configure
   frankchen@:Src$ ./configure -opensource -confirm-license \
       -release \
       -device linux-jetson-tx2-g++ \
       -device-option CROSS_COMPILE=$TX2_TOOLCHAIN \
       -sysroot $TX2_SYSROOT \
       -extprefix ~/Documents/jetson-tx2/qt5-jetson-tx2 \
       -nomake tests -nomake examples \
       -skip qtwayland -skip qtlocation -skip qtscript
   ```

   **Note:**

   > -prefix, -extprefix, and -hostprefix control the intended destination directory of the Qt build. In the above example the ARM build of Qt is expected to be placed in /usr/local/qt5 on the target device. Note that running make install does not deploy anything to the device. Instead, the install step targets the directory specified by extprefix which defaults to sysroot + prefix and is therefore optional. However, in many cases "polluting" the sysroot is not desirable and thus specifying -extprefix becomes important. Finally, -hostprefix allows separating host tools like qmake, rcc, uic from the binaries for the target. When given, such tools will be installed under the specified directory instead of extprefix.

4. make build

   ```sh
   frankchen@:Src$ make clean
   frankchen@:Src$ make -j4
   frankchen@:Src$ make install
   # the Qt libs will be installed into  `extprefix` folder
   frankchen@:Src$ ll ~/Documents/jetson-tx2/qt5-jetson-tx2/
   total 64
   drwxr-xr-x 10 frankchen frankchen  4096 Jun 20 19:20 ./
   drwxr-xr-x  4 frankchen frankchen  4096 Jun 20 17:01 ../
   drwxr-xr-x  2 frankchen frankchen  4096 Jun 20 19:20 bin/
   drwxr-xr-x  3 frankchen frankchen  4096 Jun 20 14:11 doc/
   drwxr-xr-x 76 frankchen frankchen  4096 Jun 20 19:20 include/
   drwxr-xr-x  4 frankchen frankchen 20480 Jun 20 19:20 lib/
   drwxr-xr-x 79 frankchen frankchen  4096 Jun 20 19:19 mkspecs/
   drwxr-xr-x 22 frankchen frankchen  4096 Jun 20 19:20 plugins/
   drwxr-xr-x 23 frankchen frankchen  4096 Jun 20 19:20 qml/
   drwxr-xr-x  2 frankchen frankchen 12288 Jun 20 19:20 translations/
   ```

   **Problems:**

   1. errors when building `libwebp`,

   ```sh
   frankchen@:Src$ make
   make[5]: Entering directory '/home/frankchen/Qt/5.12.3/Src/qtimageformats/src/plugins/imageformats/webp'
   /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.4.1-2017.01-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-gcc -c -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O2 -std=gnu11 -fvisibility=hidden -fno-exceptions -Wall -W -D_REENTRANT -fPIC -DQT_DEPRECATED_WARNINGS -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_NO_EXCEPTIONS -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I. -I../../../3rdparty/libwebp -I../../../3rdparty/libwebp/src -I../../../3rdparty/libwebp/src/dec -I../../../3rdparty/libwebp/src/enc -I../../../3rdparty/libwebp/src/dsp -I../../../3rdparty/libwebp/src/mux -I../../../3rdparty/libwebp/src/utils -I../../../3rdparty/libwebp/src/webp -I/home/frankchen/Qt/5.12.3/Src/qtbase/include -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtGui -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtCore -I.moc -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/libdrm -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I/home/frankchen/Qt/5.12.3/Src/qtbase/mkspecs/devices/linux-jetson-tx2-g++ -o .obj/dec_neon.o ../../../3rdparty/libwebp/src/dsp/dec_neon.c
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c: In function 'SimpleHFilter16_NEON':
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c:531:1: internal compiler error: in record_operand_use, at regrename.c:220
   }
   ^

   # enter into the folder to better tackle this issue
   frankchen@:Src$ cd /home/frankchen/Qt/5.12.3/Src/qtimageformats/src/plugins/imageformats/webp
   frankchen@:webp$ make clean
   frankchen@:webp$ /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.4.1-2017.01-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-gcc -c -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O2 -std=gnu11 -fvisibility=hidden -fno-exceptions -Wall -W -D_REENTRANT -fPIC -DQT_DEPRECATED_WARNINGS -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_NO_EXCEPTIONS -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I. -I../../../3rdparty/libwebp -I../../../3rdparty/libwebp/src -I../../../3rdparty/libwebp/src/dec -I../../../3rdparty/libwebp/src/enc -I../../../3rdparty/libwebp/src/dsp -I../../../3rdparty/libwebp/src/mux -I../../../3rdparty/libwebp/src/utils -I../../../3rdparty/libwebp/src/webp -I/home/frankchen/Qt/5.12.3/Src/qtbase/include -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtGui -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtCore -I.moc -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/libdrm -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I/home/frankchen/Qt/5.12.3/Src/qtbase/mkspecs/devices/linux-jetson-tx2-g++ -o .obj/dec_neon.o ../../../3rdparty/libwebp/src/dsp/dec_neon.c
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c: In function 'SimpleHFilter16_NEON':
   ../../../3rdparty/libwebp/src/dsp/dec_neon.c:531:1: internal compiler error: in record_operand_use, at regrename.c:220
   }
   ^
   Please submit a full bug report,
   with preprocessed source if appropriate.
   See <http://gcc.gnu.org/bugs.html> for instructions.


   # possible solution, using the linaro toolchain with new version(5.5.0-2017.10) maybe fix the bug
   frankchen@:webp$ make clean
   frankchen@:webp$ /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-gcc -c -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O2 -std=gnu11 -fvisibility=hidden -fno-exceptions -Wall -W -D_REENTRANT -fPIC -DQT_DEPRECATED_WARNINGS -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_NO_EXCEPTIONS -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DQT_PLUGIN -DQT_GUI_LIB -DQT_CORE_LIB -I. -I../../../3rdparty/libwebp -I../../../3rdparty/libwebp/src -I../../../3rdparty/libwebp/src/dec -I../../../3rdparty/libwebp/src/enc -I../../../3rdparty/libwebp/src/dsp -I../../../3rdparty/libwebp/src/mux -I../../../3rdparty/libwebp/src/utils -I../../../3rdparty/libwebp/src/webp -I/home/frankchen/Qt/5.12.3/Src/qtbase/include -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtGui -I/home/frankchen/Qt/5.12.3/Src/qtbase/include/QtCore -I.moc -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/libdrm -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I/home/frankchen/Qt/5.12.3/Src/qtbase/mkspecs/devices/linux-jetson-tx2-g++ -o .obj/dec_neon.o ../../../3rdparty/libwebp/src/dsp/dec_neon.c

   ```

   similiar problems found online:

   - (Internal compiler error using -mtune=cortex-a57.cortex-a53 with linaro gcc 5.2.1)[https://bugs.linaro.org/show_bug.cgi?id=2785]
   - (Errors buliding libwebp on NVIDIA TX2 with Linaro gcc-5.4.0 using flags)[https://github.com/opencv/opencv/issues/12322]
   - (internal compiler error in record_operand_use)[https://www.mail-archive.com/gcc-bugs@gcc.gnu.org/msg472065.html]

   1. stdlib.h

   ```sh
   make[3]: Entering directory '/home/frankchen/Qt/5.12.3/Src/qtbase/src/corelib'
   /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/bin/aarch64-linux-gnu-g++ -pipe -mtune=cortex-a57.cortex-a53 -march=armv8-a --sysroot=/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs -O3 -std=c++1y -fvisibility=hidden -fvisibility-inlines-hidden -Wall -W -Wvla -Wdate-time -D_REENTRANT -fPIC -DQT_NO_USING_NAMESPACE -DQT_NO_FOREACH -DQT_NO_NARROWING_CONVERSIONS_IN_CONNECT -DQT_BUILD_CORE_LIB -DQT_BUILDING_QT -DQT_NO_CAST_TO_ASCII -DQT_ASCII_CAST_WARNINGS -DQT_MOC_COMPAT -DQT_USE_QSTRINGBUILDER -DQT_DEPRECATED_WARNINGS -DQT_DISABLE_DEPRECATED_BEFORE=0x050000 -D_LARGEFILE64_SOURCE -D_LARGEFILE_SOURCE -DQT_NO_DEBUG -DPCRE2_CODE_UNIT_WIDTH=16 -I. -Iglobal -I../3rdparty/harfbuzz/src -I../3rdparty/md5 -I../3rdparty/md4 -I../3rdparty/sha3 -I../3rdparty -I../3rdparty/double-conversion/include -I../3rdparty/double-conversion/include/double-conversion -I../3rdparty/forkfd -I../3rdparty/tinycbor/src -I../../include -I../../include/QtCore -I../../include/QtCore/5.12.3 -I../../include/QtCore/5.12.3/QtCore -I.moc -I.tracegen -I../3rdparty/pcre2/src -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/glib-2.0 -I/home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/lib/aarch64-linux-gnu/glib-2.0/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include -isystem /home/frankchen/nvidia/nvidia_sdk/JetPack_4.2_Linux_P3310/Linux_for_Tegra/rootfs/usr/include/aarch64-linux-gnu -I../../mkspecs/devices/linux-jetson-tx2-g++ -x c++-header -c global/qt_pch.h -o .pch/Qt5Core.gch/c++
   In file included from /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/aarch64-linux-gnu/include/c++/7.4.1/bits/stl_algo.h:59:0,
                   from /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/aarch64-linux-gnu/include/c++/7.4.1/algorithm:62,
                   from global/qglobal.h:142,
                   from global/qt_pch.h:56:
   /home/frankchen/Documents/jetson-tx2/toolchains/gcc-linaro-7.4.1-2019.02-x86_64_aarch64-linux-gnu/aarch64-linux-gnu/include/c++/7.4.1/cstdlib:75:15: fatal error: stdlib.h: No such file or directory
   #include_next <stdlib.h>
               ^~~~~~~~~~
   # possible solution, using the linaro toolchain with new version(5.5.0-2017.10) maybe fix the bug
   ```

5. build a `Qt` application for `Jetson TX2` on linux host

   ```sh
   # cd <Project folder>
   frankchen@:build-TextFinder-JetsonTx2$ cd ~/Documents/qt-project/
   frankchen@:qt-project$ ll
   total 32
   drwxr-xr-x  8 frankchen frankchen 4096 Jun 21 11:00 ./
   drwxrwxrwx 26 frankchen frankchen 4096 Jun 18 17:11 ../
   drwxrwxr-x  2 frankchen frankchen 4096 Jun 13 15:12 build-TextFinder-Android_for_arm64_v8a_Clang_Qt_5_12_3_for_Android_ARM64_v8a-Release/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 12 12:50 build-TextFinder-Desktop_Qt_5_12_3_GCC_64bit-Release/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 12 16:26 build-TextFinder-Desktop_Qt_5_12_3_Win/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 21 11:03 build-TextFinder-JetsonTx2/
   drwxr-xr-x  2 frankchen frankchen 4096 Jun 17 16:39 build-TextFinder-RaspberryPi/
   drwxrwxr-x  2 frankchen frankchen 4096 Jun 13 15:12 TextFinder/

   # create build folder and cd into
   frankchen@:qt-project$ mkdir build-TextFinder-JetsonTx2
   frankchen@:qt-project$ cd build-TextFinder-JetsonTx2/

   # create `Makefile` using `qmake` tool
   frankchen@:build-TextFinder-JetsonTx2$ "/home/frankchen/Documents/jetson-tx2/qt5-jetson-tx2/bin/qmake" /home/frankchen/Documents/qt-project/TextFinder/TextFinder.pro

   # build executable file
   frankchen@:build-TextFinder-JetsonTx2$ make -j4
   frankchen@:build-TextFinder-JetsonTx2$ file TextFinder
   TextFinder: ELF 64-bit LSB executable, ARM aarch64, version 1 (SYSV), dynamically linked, interpreter /lib/ld-, for GNU/Linux 3.7.0, BuildID[sha1]=248f556bb9b9dfa0329b54b918f919ce406da67b, not stripped
   ```

**References:**

- [NVIDIA JetPack Software](https://developer.nvidia.com/embedded/develop/software)
- [CUDA Development for Jetson with NVIDIA Nsight Eclipse Edition](https://devblogs.nvidia.com/cuda-jetson-nvidia-nsight-eclipse-edition/)
