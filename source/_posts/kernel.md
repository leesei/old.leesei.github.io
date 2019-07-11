---
title: Kernel
categories:
  - comp
tags:
  - linux
  - unikernel
  - microkernel
toc: true
date: 2016-03-27 22:38:28
---

> include `rtos.md`

## Operating Systems

[Think OS – Green Tea Press](http://greenteapress.com/wp/think-os/)
[cs4414: Operating Systems](http://rust-class.org/index.html) write a kernel in Rust

[Workplace OS History: IBM’s \$2 Billion Microkernel of Failure](https://tedium.co/2019/02/28/ibm-workplace-os-taligent-history/) OS2

[achilleasa/gopher-os: A proof of concept OS kernel written in Go](https://github.com/achilleasa/gopher-os)
[jjyr/bootgo: A barebones OS kernel written in go](https://github.com/jjyr/bootgo)

[Operating Systems and Middleware: Supporting Controlled Interaction](https://gustavus.edu/mcs/max/os-book/) stopped updating

[Optimizing for Workloads: Linux Spinlocks vs. Mutexes | Nathan Petersen](https://nathanpetersen.com/2019/02/17/optimizing-for-workloads-linux-spinlocks-vs-mutexes/)

## Linux Kernel

[Linux kernel - Wikiwand](https://www.wikiwand.com/en/Linux_kernel)
[Anatomy of the Linux kernel](https://www.ibm.com/developerworks/library/l-linux-kernel/)
[25 Years Later: Interview with Linus Torvalds | Linux Journal](https://www.linuxjournal.com/content/25-years-later-interview-linus-torvalds)
[10 moments that shaped Linux history | Opensource.com](https://opensource.com/article/19/4/top-moments-linux-history?utm_campaign=intrel)

[Welcome to LWN.net [LWN.net]](https://lwn.net/)
[Linux Kernel Newbies - Linux Kernel Newbies](https://kernelnewbies.org/)
[Exploring the Linux kernel: The secrets of Kconfig/kbuild | Opensource.com](https://opensource.com/article/18/10/kbuild-and-kconfig)

[What are good ways to understand the Linux kernel? - Quora](https://www.quora.com/What-are-good-ways-to-understand-the-Linux-kernel)
[What is a Linux 'oops'? | Network World](https://www.networkworld.com/article/3254778/linux/what-is-a-linux-oops.html)
[Difference Between the macOS and Linux Kernels [Explained] | It's FOSS](https://itsfoss.com/mac-linux-difference/)

### Books

[Linux Inside · GitBook](https://www.gitbook.com/book/0xax/linux-insides/details)
[Linux Kernel in a Nutshell](http://www.kroah.com/lkn/) 2.6.18 @2006
[Linux Device Drivers, Third Edition [LWN.net]](https://lwn.net/Kernel/LDD3/) 2.6.10 @2005

### Compression

[Ubuntu Moving Ahead With Compressing Their Kernel Image Using LZ4 - Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=LZ4-Initramfs-Ubuntu-Go-Ahead)
[Facebook Looking To Add Zstd Support To The Linux Kernel, Btrfs - Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=Facebook-Linux-Zstd)

As used by mkinitramfs:

- lz4 is faster to compress than gzip
- lz4 is blazingly fast to decompress
- lzma is dog slow to compress and decompress, but is tiny
- lz4 size weight over gzip is marginal (14%) but imho worth the improved boot time & initrd creation time
- xz is potentially even slower and even smaller than lzma
- zstd compress at speeds approaching lz4, decompressions at speeds more than twice as fast as zlib, and quality approaching lzma

### Device Drivers

[Writing a Linux Kernel Module — Part 1: Introduction | derekmolloy.ie](http://derekmolloy.ie/writing-a-linux-kernel-module-part-1-introduction/)
[Writing a Linux Kernel Module — Part 2: A Character Device | derekmolloy.ie](http://derekmolloy.ie/writing-a-linux-kernel-module-part-2-a-character-device/)
[Writing a Linux Loadable Kernel Module (LKM) - Interfacing to GPIOs | derekmolloy.ie](http://derekmolloy.ie/kernel-gpio-programming-buttons-and-leds/)
[Writing a Linux Loadable Kernel Module (LKM) - Interfacing to GPIOs | derekmolloy.ie](http://derekmolloy.ie/kernel-gpio-programming-buttons-and-leds/)
[exploringBB/extras/kernel at master · derekmolloy/exploringBB](https://github.com/derekmolloy/exploringBB/tree/master/extras/kernel/)

### DKMS

[Dynamic Kernel Module Support - Wikiwand](https://www.wikiwand.com/en/Dynamic_Kernel_Module_Support)
[Dynamic Kernel Module Support - ArchWiki](https://wiki.archlinux.org/index.php/Dynamic_Kernel_Module_Support)
[Kernel Korner - Exploring Dynamic Kernel Module Support (DKMS) | Linux Journal](https://www.linuxjournal.com/article/6896)

Recompiles drivers against kernel header on host on every driver update OR kernel update.

### Device Tree

[Index of /doc/Documentation/devicetree/](https://www.kernel.org/doc/Documentation/devicetree/)
[Device tree - Wikiwand](https://www.wikiwand.com/en/Device_tree)

[Device Tree Tutorial (ARM) – Linux Kernel For Newbies](https://saurabhsengarblog.wordpress.com/2015/11/28/device-tree-tutorial-arm/)
[Device Tree Reference - eLinux.org](https://elinux.org/Device_Tree_Reference)
[Device Tree for Dummies](https://elinux.org/images/f/f9/Petazzoni-device-tree-dummies_0.pdf) (PDF)

[A Tutorial on the Device Tree (Zynq) -- Part I | xillybus.com](http://xillybus.com/tutorials/device-tree-zynq-1)
[A Tutorial on the Device Tree (Zynq) -- Part II | xillybus.com](http://xillybus.com/tutorials/device-tree-zynq-2)
[A Tutorial on the Device Tree (Zynq) -- Part III | xillybus.com](http://xillybus.com/tutorials/device-tree-zynq-3)
[A Tutorial on the Device Tree (Zynq) -- Part IV | xillybus.com](http://xillybus.com/tutorials/device-tree-zynq-4)
[A Tutorial on the Device Tree (Zynq) -- Part V | xillybus.com](http://xillybus.com/tutorials/device-tree-zynq-5)

### GPIO/sysfs

One way of accessing GPIO is to modify the device tree and write a device driver for it.
We could also expose the GPIO via Sysfs interface ("pinctrl" driver) (`/sys/class/gpio`) to allow access on user space.

[GPIO - eLinux.org](https://elinux.org/GPIO)
[Access GPIO from Linux user space](https://falsinsoft.blogspot.com/2012/11/access-gpio-from-linux-user-space.html)
[Working with GPIO on the Wandboard and Writing an Android Driver for GPIO Interrupts – Using Android in Industrial Automation](http://android.serverbox.ch/?p=972) with `poll()`
[关于 /sys/class/gpio 简介 - cjsycyl 的专栏 - CSDN 博客](https://blog.csdn.net/cjsycyl/article/details/46310939)
[GPIO 接口解析-wangbaolin719-ChinaUnix 博客](http://blog.chinaunix.net/uid-27717694-id-3701921.html)
[Controlling GPIO from Linux User Space](https://www.emcraft.com/stm32f429discovery/controlling-gpio-from-linux-user-space)
[RK3399 用户空间 IO 控制 - zhuyong006 的博客 - CSDN 博客](https://blog.csdn.net/zhuyong006/article/details/80907718?utm_source=blogxgwz0)

[Index of /doc/Documentation/gpio/](https://www.kernel.org/doc/Documentation/gpio/)
[https://www.kernel.org/doc/Documentation/gpio/sysfs.txt](https://www.kernel.org/doc/Documentation/gpio/sysfs.txt) Sysfs GPIO interface is deprecated
[https://www.kernel.org/doc/Documentation/gpio/gpio-legacy.txt](https://www.kernel.org/doc/Documentation/gpio/gpio-legacy.txt)
[https://www.kernel.org/doc/Documentation/ABI/obsolete/sysfs-gpio](https://www.kernel.org/doc/Documentation/ABI/obsolete/sysfs-gpio)
[linux/tools/gpio at master · torvalds/linux](https://github.com/torvalds/linux/tree/master/tools/gpio) new interface

[vitiral/gpio: python gpio module for linux using the sysfs file access (/sys/class/gpio). Mimics similar Raspberry Pi IO libraries](https://github.com/vitiral/gpio)

```sh
# get GPIO number in kernel
# 1. refer to spec
# 2. check debug info
cat /sys/kernel/debug/gpio

# export a GPIO pin to userspace
echo $GPIO_NUMBER > /sys/class/gpio/export

echo $GPIO_DIRECTION > /sys/class/gpio/gpio$GPIO_NUMBER/direction  # "in" or "out"
# read and write to pin
cat /sys/class/gpio/gpio$GPIO_NUMBER/value
echo 1 > /sys/class/gpio/gpio$GPIO_NUMBER/value

# clean up
echo $GPIO_NUMBER > /sys/class/gpio/unexport
```

```sh
# debug
mount -t debugfs debugfs /sys/kernel/debug
cat /sys/kernel/debug/gpio
```

### I2C

[Index of /doc/Documentation/i2c/](https://www.kernel.org/doc/Documentation/i2c/)
[https://www.kernel.org/doc/Documentation/i2c/smbus-protocol](https://www.kernel.org/doc/Documentation/i2c/smbus-protocol)
On Linux with proper driver installed, it is exposed as `/dev/i2c-N`

[bjornt/pysmbus](https://github.com/bjornt/pysmbus)
[kplindegaard/smbus2: A drop-in replacement for smbus-cffi/smbus-python in pure Python](https://github.com/kplindegaard/smbus2)

### SPI

[Index of /doc/Documentation/spi/](https://www.kernel.org/doc/Documentation/spi/)
[https://www.kernel.org/doc/Documentation/spi/spi-summary](https://www.kernel.org/doc/Documentation/spi/spi-summary)

On Linux with proper driver installed, it is exposed as `/dev/spidevX.Y`

### Video Driver

Proprietary (non-free) drivers is a source of problem. You will have to rebuild the driver every time the kernel is updated. Otherwise X will fail to start.
If performance is not an issue it is [recommended](https://wiki.archlinux.org/index.php/Enhance_system_stability#Choose_open-source_drivers) to use the free drivers.

[Bumblebee - ArchWiki](https://wiki.archlinux.org/index.php/bumblebee)

#### Hybrid graphics

[Hybrid graphics - ArchWiki](https://wiki.archlinux.org/index.php/hybrid_graphics)
[Bumblebee - ArchWiki](https://wiki.archlinux.org/index.php/bumblebee)
[NVIDIA Optimus - ArchWiki](https://wiki.archlinux.org/index.php/NVIDIA_Optimus)

[Optimus Technology|NVIDIA](https://www.nvidia.com/object/optimus_technology.html)
[HybridGraphics - Community Help Wiki](https://help.ubuntu.com/community/HybridGraphics)
[How To Switch Between Intel and Nvidia Graphics Card on Ubuntu](https://www.linuxbabe.com/desktop-linux/switch-intel-nvidia-graphics-card-ubuntu)

[The State of NVIDIA Optimus on Linux | The Linux Rain](http://www.thelinuxrain.com/articles/the-state-of-nvidia-optimus-on-linux)

[wildtruc/nvidia-prime-select: This a fork of FedoraPrime enhanced for all linux distributions](https://github.com/wildtruc/nvidia-prime-select)

### File Locks

[flock - apply or remove an advisory lock on an open file](https://www.mankier.com/2/flock) ("BSD Locks")
[fcntl - manipulate file descriptor - System Calls | ManKier](https://www.mankier.com/2/fcntl) ("POSIX Locks")

[lockf - apply, test or remove a POSIX lock on an open file](https://www.mankier.com/3/lockf)
[lsof - list open files - man page | ManKier](https://www.mankier.com/1/lsof)

Checking locked files:

```sh
sudo lsof -n <file>
sudo lsof +f -- /dev/mapper/cachedev1
```

### udev

[udev - ArchWiki](https://wiki.archlinux.org/index.php/Udev)
[Writing udev rules](http://www.reactivated.net/writing_udev_rules.html)
[Scripting with udev - jasonwryan.com](http://jasonwryan.com/blog/2014/01/20/udev/)

### procfs

[/proc Talk » Linux Magazine](http://www.linuxpromagazine.com/Issues/2018/217/Exploring-proc/)

### RPi

[Department of Computer Science and Technology – Raspberry Pi: Baking Pi – Operating Systems Development](https://www.cl.cam.ac.uk/projects/raspberrypi/tutorials/os/)
[Tutorial | Building an Operating System for the Raspberry Pi](https://jsandler18.github.io/)
[dwelch67/raspberrypi: Raspberry Pi ARM based bare metal examples](https://github.com/dwelch67/raspberrypi)

## Unikernel

[Unikernel - Wikiwand](https://www.wikiwand.com/en/Unikernel)

[oscarlab/graphene: Graphene / Graphene-SGX Library OS - a library OS for Linux multi-process applications, with Intel SGX support](https://github.com/oscarlab/graphene)
[Mini-OS-DevNotes - Xen](https://wiki.xenproject.org/wiki/Mini-OS-DevNotes)

[Unikernels [Book]](https://www.safaribooksonline.com/library/view/unikernels/9781492042815/)

[Joyent | Unikernels are unfit for production](https://www.joyent.com/blog/unikernels-are-unfit-for-production)

### Unikernel

[Unikernels - Rethinking Cloud Infrastructure](http://unikernel.org/) (bought by Docker)
[Projects | Unikernels](http://unikernel.org/projects/) Kernel as a lib

[Unikernel Systems Joins Docker | Docker Blog](https://blog.docker.com/2016/01/unikernel/)
[Docker’s Unikernel Experiment Begins Paying Off with Mac OS Libraries - The New Stack](http://thenewstack.io/dockers-unikernel-experiment-begins-paying-off-mac-os-libraries/)
[Improving Docker with Unikernels: Introducing HyperKit, VPNKit and DataKit | Docker Blog](https://blog.docker.com/2016/05/docker-unikernels-open-source/)
[docker/hyperkit: A toolkit for embedding hypervisor capabilities in your application](https://github.com/docker/hyperkit)

[IncludeOS](http://www.includeos.org/)

[Unikernels with Idit Levine | Software Engineering Daily](http://softwareengineeringdaily.com/2016/09/14/unikernels-with-idit-levine/) Mirage, Rump, UniK

### MirageOS

[MirageOS](https://mirage.io/) build unikernel for network applications, deploy minimum app, written in OCaml
[Episode 204: Anil Madhavapeddy on the Mirage Cloud Operating System and the OCaml Language : Software Engineering Radio](http://www.se-radio.net/2014/05/episode-204-anil-madhavapeddy-on-the-mirage-cloud-operating-system-and-the-ocaml-language/)
[My Other Internet is a Mirage](https://www.infoq.com/presentations/mirage-os)

Boots domain 0 OS

### Rump

POSIX compatible unikernel
[Rump Kernels](http://rumpkernel.org/)
[rumpkernel/rumprun: The Rumprun unikernel and toolchain for various platforms](https://github.com/rumpkernel/rumprun)

### UniK

[unikernels and unik with Scott Weiss | Software Engineering Daily](http://softwareengineeringdaily.com/2016/08/11/unikernels-and-unik-with-scott-weiss/)

[emc-advanced-dev/unik: The Unikernel Compilation and Deployment Platform](https://github.com/emc-advanced-dev/unik) Kubernetes for unikernel, supports different providers

[Unikernel power comes to Java, Node.js, Go, and Python apps | InfoWorld](http://www.infoworld.com/article/3082051/open-source-tools/unikernel-power-comes-to-java-nodejs-go-and-python-apps.html)

## Light kernel

> see `rtos.md`
> see `mobile-os.md#google-fuchsia`

[littlekernel/lk: LK embedded kernel](https://github.com/littlekernel/lk)

## Microkernel

[Microkernel - Wikiwand](https://www.wikiwand.com/en/Microkernel)
[Is Linux kernel design outdated? : linux](https://www.reddit.com/r/linux/comments/69umqo/is_linux_kernel_design_outdated/)
