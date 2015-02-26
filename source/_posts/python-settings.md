title: Python settings
toc: true
date: 2014-12-11 17:27:59
tags:
- python
- settings
- pip
- package-manager
---

# Python settings

## Installing pip

http://www.pip-installer.org/en/latest/installing.html

### from package manager
```bash
sudo apt-get install python-pip
```

### latest
```bash
sudo -v
curl -OL https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py
sudo python ez_setup.py
curl -OL https://raw.github.com/pypa/pip/master/contrib/get-pip.py
sudo python get-pip.py
```

## Packages

```bash
sudo pip install httpie pygments
sudo pip install asciinema TermRecord
sudo pip install landslide
```

```bash
sudo apt-get install ipython python-pygame
```

## virtualenv

> it is a little troublesome to setup

http://webapp-improved.appspot.com/tutorials/virtualenv.html
http://code4reference.com/2014/05/python-virtual-environment/

```bash
sudo pip install virtualenv
source virtualenv-auto-activate.sh in .bashrc
```

Usage:

```bash
# create env in current directory
virtualenv env
. env/bin/activate
pip install -r requirements.txt  # if any
deactivate
```

## List installed packages

```bash
pip list
pip freeze
```
