---
title: Vagrant
categories:
  - app
tags:
  - vagrant
toc: true
date: 2017-06-04 19:01:13
---

# Vagrant

Create and configure lightweight, reproducible, and portable development environments.

[Vagrant by HashiCorp](https://www.vagrantup.com/)
[Vagrant Documentation](https://docs.vagrantup.com/)
[Command-Line Interface - Vagrant by HashiCorp](https://www.vagrantup.com/docs/cli/)

```sh
# 'box' equals virtual machine image
vagrant box add ubuntu/trusty64

mkdir trusty64 && cd trusty64
# init a project from box, configuration in `Vagrantfile`
vagrant init ubuntu/trusty64
# start an instance with the `Vagrantfile`
vagrant up --provider virtualbox
# `pwd` is mounted to /vagrant
vagrant destroy
```

[Getting Started with Vagrant](https://coolaj86.com/articles/getting-started-with-vagrant.html)
[How to Create a Vagrant Base Box from an Existing One ♥ Scotch](http://scotch.io/tutorials/how-to-create-a-vagrant-base-box-from-an-existing-one)
[Vagrant Cloud](https://vagrantcloud.com/)
[Vargant一个属于程序员的虚拟机 | YL Notes](http://yunlzheng.github.io/2013/11/26/cool-vagrant/)
[Easy Node.js Development Environment With Vagrant - Tuts+ Course](https://code.tutsplus.com/courses/easy-nodejs-development-environment-with-vagrant)

## Vagrantfile

[Vagrantfile - Vagrant by HashiCorp](https://www.vagrantup.com/docs/vagrantfile/)

## Building Vagrant box

[Creating a Base Box - Vagrant by HashiCorp](https://www.vagrantup.com/docs/boxes/base.html)
[Building a Vagrant Box from Start to Finish](https://blog.engineyard.com/2014/building-a-vagrant-box)

[GitHub - jedi4ever/veewee: Easing the building of vagrant boxes](https://github.com/jedi4ever/veewee)
