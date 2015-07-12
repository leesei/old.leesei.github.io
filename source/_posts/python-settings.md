title: "Python settings"
date: 2014-12-11 17:27:59
categories:
- comp.lang
tags:
- python
- settings
- pip
- package-manager
toc: true
---

## Installing pip

http://www.pip-installer.org/en/latest/installing.html

### from package manager
```sh
sudo apt-get install python-pip
```

### latest
```sh
sudo -v
curl -OL https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py
sudo python ez_setup.py
curl -OL https://raw.github.com/pypa/pip/master/contrib/get-pip.py
sudo python get-pip.py
```

## Packages

```sh
sudo pip install httpie pygments
sudo pip install asciinema TermRecord
sudo pip install landslide
sudo pip install git-up
```

```sh
sudo apt-get install ipython python-pygame
```

## virtualenv

> it is a little troublesome to setup

http://webapp-improved.appspot.com/tutorials/virtualenv.html
http://code4reference.com/2014/05/python-virtual-environment/

```sh
sudo pip install virtualenv
source virtualenv-auto-activate.sh in .bashrc
```

Usage:

```sh
# create env in current directory
virtualenv env
. env/bin/activate
pip install -r requirements.txt  # if any
deactivate
```

## List installed packages

```sh
pip list
pip freeze
```
