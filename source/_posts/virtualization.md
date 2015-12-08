---
title: "Virtualization"
date: 2015-05-10 17:03:12
categories:
- linux
tags:
- virtualbox
- vagrant
- chef
toc: true
---

## VirtualBox

[Downloads – Oracle VM VirtualBox](https://www.virtualbox.org/wiki/Downloads)
Also download the extension packs (PUEL, non-commercial only).

### Enable 64-bit support

> [virtualbox.org • View topic - I have a 64bit host, but can't install 64bit guests](https://forums.virtualbox.org/viewtopic.php?f=1&t=62339)

To enable 64bit guests, run through the following checklist:

1. Note your exact CPU model or part number, then go online and check its capabilities. The CPU must have 64bit capability and support either Intel or AMD virtualization technologies: VT-x or AMD-v.

2. You usually need to enable VT-x/AMD-v in the host PC BIOS. You need to check with your PC manual or support forum to find out how to boot into the BIOS screen. This is not something we here at the forums can help you with. Once you get there you need to look for something buried in a menu, perhaps in the security category. The option may be called something like "Enable Virtualization Technology". If you see "Virtual Directed I/O" then that is a different thing. Remember to reboot your host OS after making BIOS changes - in this case a full restart from power off is required, just resuming from a hibernated state may not do the job.

3. If (1) and (2) are already taken care of, then make sure that no other host apps are already using VT-x/AMD-v. The usual culprits are system level debuggers, other VM platforms, and some resident anti-virus applications. This has become a particular issue with 64bit Windows desktop and server hosts - especially Win8/Win2k12/Win10, since these may enable Microsoft's Hyper-v VM platform by default: this grabs ownership of VT-x and won't play nice with VirtualBox.

4. When creating a VM, make sure you choose the 64-bit version of the guest OS template in <VM Settings> | General | Basic | Version, e.g. choose "Ubuntu (64 bit)" and not "Ubuntu" or "Ubuntu (32bit)". This has become more important since VirtualBox 4.3.x, because choosing the correct template also allows other modern processor features to be visible to the guest - it's not just about 64bit capability any more.

## Vagrant

[Vagrant](https://www.vagrantup.com/)


## Chef

[Chef | IT automation for speed and awesomeness | Chef](https://www.chef.io/chef/)
[jimeh/chef-simple_users](https://github.com/jimeh/chef-simple_users)

## devbox

Script that uses Vagrant and Chef to setup a VM.
[jimeh/devbox](https://github.com/jimeh/devbox)
