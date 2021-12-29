---
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

## Package Manager

[Installing Packages — Python Packaging User Guide](https://packaging.python.org/tutorials/installing-packages/)
[Installing Python Modules — Python documentation](https://docs.python.org/latest/installing/index.html)
[PyPI - the Python Package Index : Python Package Index](https://pypi.python.org/pypi)
[Python Wheels](http://pythonwheels.com/)
[What Is Pip? A Guide for New Pythonistas – Real Python](https://realpython.com/what-is-pip/)
[Python Application Dependency Management in 2018 · Homepage of Hynek Schlawack](https://hynek.me/articles/python-app-deps-2018/)

Python look up packages in this order:

- user path
- site path
- system path

On Windows Python loads according to `%PATH%` variable.

```python
python -c "import site; print(site.getsitepackages())"
```

[Presentations & Blog Posts — Conda documentation](http://conda.pydata.org/docs/)
[Anaconda Distribution | Continuum Analytics: Documentation](https://docs.continuum.io/anaconda/)

[Python Module of the Week - Python Module of the Week](https://pymotw.com/2/index.html)
[Python 3 Module of the Week — PyMOTW 3](https://pymotw.com/3/)
[dhellmann / PyMOTW-3 — Bitbucket](https://bitbucket.org/dhellmann/pymotw-3/)

[pipx · PyPI](https://pypi.org/project/pipx/) installs to virtualenv

[A Better Pip Workflow™ — Kenneth Reitz](https://www.kennethreitz.org/essays/a-better-pip-workflow)
[Pin Your Packages » nvie.com](https://nvie.com/posts/pin-your-packages/)
[The Nine Circles of Python Dependency Hell – Knerd – Medium](https://medium.com/knerd/the-nine-circles-of-python-dependency-hell-481d53e3e025)

`pip` issues:

- non-deterministic build (without pinning)
- manual update of sub-dependencies (with pinning)
- global dependencies (solved with virtual env)
- no dependency resolution

### Installing pip

[pip — documentation](https://pip.pypa.io/en/stable/)
[Installation — pip documentation](https://pip.pypa.io/en/latest/installing.html)

#### latest

```sh
sudo -v
curl -OL https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py
sudo python ez_setup.py
curl -OL https://bootstrap.pypa.io/get-pip.py
sudo python get-pip.py
```

### `pip` Usage

```sh
pip install package
# show all versions on PyPI
pip install package==
# install a particular version
pip install package==0.1.2

# upgrade package
pip install -U package
pip install --upgrade package

# generate requirements.txt
pip freeze > requirements.txt
# install from requirements.txt
pip install --no-cache-dir -r requirements.txt

# Useful for containers:
--disable-pip-version-check
--no-cache-dir
```

### conditions in `requirements.txt`

[pip - Is there a way to have a conditional requirements.txt file for my Python application based on platform? - Stack Overflow](https://stackoverflow.com/questions/29222269/is-there-a-way-to-have-a-conditional-requirements-txt-file-for-my-python-applica)
[PEP 508 -- Dependency specification for Python Software Packages | Python.org](https://www.python.org/dev/peps/pep-0508/)

```
package1==0.0.1; platform_system != "Windows"
package2==0.0.1; python_version < '3.7' and
```

### `pip-tools`

> principals adopted by `pipenv`

[jazzband/pip-tools: A set of tools to keep your pinned Python dependencies fresh.](https://github.com/jazzband/pip-tools)

[Better Package Management » nvie.com](https://nvie.com/posts/better-package-management/)

### Poetry

[Poetry - Python dependency management and packaging made easy.](https://poetry.eustace.io/)
[sdispater/poetry: Python dependency management and packaging made easy.](https://github.com/sdispater/poetry) also build and publish packages

[Dependency Management With Python Poetry – Real Python](https://realpython.com/dependency-management-python-poetry/)

## Virtual Environments

> use `pipenv`, `pyenv virtualenv`

[Python Virtual Environments: A Primer – Real Python](https://realpython.com/python-virtual-environments-a-primer/)
[An Effective Python Environment: Making Yourself at Home – Real Python](https://realpython.com/effective-python-environment/)

[28.3. venv — Creation of virtual environments — Python documentation](https://docs.python.org/3/library/venv.html)
[Virtualenv — virtualenv documentation](https://virtualenv.pypa.io/en/latest/)
[Deepwalker/pundler: Python bundler-alike alternative to virtualenv](https://github.com/Deepwalker/pundler)

[Create Virtual Environment using “virtualenv” and add it to Jupyter Notebook | by B. Chen | Towards Data Science](https://towardsdatascience.com/create-virtual-environment-using-virtualenv-and-add-it-to-jupyter-notebook-6e1bf4e03415)
[Python virtualenv and venv do’s and don’ts | InfoWorld](https://www.infoworld.com/article/3306656/python-virtualenv-and-venv-dos-and-donts.html)
[Virtualenv and venv: Python virtual environments explained | InfoWorld](https://www.infoworld.com/article/3239675/python/virtualenv-and-venv-python-virtual-environments-explained.html)
[pyvenv vs virtualenv : learnpython](https://www.reddit.com/r/learnpython/comments/4hsudz/pyvenv_vs_virtualenv/)

[Pipenv: A Guide to the New Python Packaging Tool – Real Python](https://realpython.com/pipenv-guide/)
[An Effective Python Environment: Making Yourself at Home – Real Python](https://realpython.com/effective-python-environment/)
[Python Virtual Environments – A Primer – Real Python](https://realpython.com/python-virtual-environments-a-primer/)
[Using virtual environments with Python ~ The Python Corner](https://www.thepythoncorner.com/2018/05/using-virtual-environments-withpython.html)

[A Minimalist Approach to Python Virtual Environments](https://towardsdatascience.com/a-minimalist-approach-to-python-virtual-environments-f5dacf76bfad)
[willcasey/venvtool](https://github.com/willcasey/venvtool)

### pipenv

`pipenv` is the recommend package management tool by PyPA and the reference implementation for [Pipfile](https://github.com/pypa/pipfile) (`requirements.txt` replacement). It creates virtualenv in `~/.local/share/virtualenvs` instead of project folder.

[Pipenv: Python Dev Workflow for Humans — pipenv documentation](https://pipenv.pypa.io/en/latest/)
[pypa/pipenv: Python Development Workflow for Humans.](https://github.com/pypa/pipenv)
[Kenneth Reitz - Pipenv: The Future of Python Dependency Management - PyCon 2018 - YouTube](https://www.youtube.com/watch?v=GBQAKldqgZs)

[Pipenv: A Guide to the New Python Packaging Tool – Real Python](https://realpython.com/pipenv-guide/)

[Why you should use pyenv + Pipenv for your Python projects](https://hackernoon.com/reaching-python-development-nirvana-bb5692adf30c) !important
[The Python virtual environment with Pyenv & Pipenv - DEV Community 👩‍💻👨‍💻](https://dev.to/writingcode/the-python-virtual-environment-with-pyenv-pipenv-3mlo)
[Python Environment 101. How are pyenv and pipenv different and… | by Shinichi Okada | Towards Data Science](https://towardsdatascience.com/python-environment-101-1d68bda3094d)
[Pyenv support broken since version 2018.10.09 ? · Issue #3136 · pypa/pipenv](https://github.com/pypa/pipenv/issues/3136)

Issues:

- for application only, not for libraries
- py2 and py3 cannot co-exist
- locked to a single minor version of Python  
  often reporting version mismatch when running script in other environment
- no QA before release
- [Why is pipenv the recommended packaging tool by the community and PyPA? : Python](https://www.reddit.com/r/Python/comments/8jd6aq/why_is_pipenv_the_recommended_packaging_tool_by/)
- [Pyenv support broken · Issue #3551 · pypa/pipenv](https://github.com/pypa/pipenv/issues/3551)
  `pip install -e git+https://github.com/pypa/pipenv.git@master#egg=pipenv`  
  `pip install --upgrade https://github.com/pypa/pipenv/archive/master.zip`
- [different package versions for different python versions · Issue #2171 · pypa/pipenv](https://github.com/pypa/pipenv/issues/2171)  
  [Creating a Pipfile which has different installation instructions depending on operating systems (PyTorch v0.4.1 as an example) - DEV Community](https://dev.to/tomoyukiaota/creating-a-pipfile-which-has-different-installation-instructions-depending-on-operating-systems-pytorch-v041-as-an-example-56i8)

```sh
# enter the virtualenv (automatically create Pipfile)
pipenv shell

# force use your host's Python if the Python version mismatch with Pipfile
# warning: the script may use features not available on your host's Python
pipenv --python $(which python3) shell
pipenv --python $(which python2) shell

# install dependencies with `pipenv` instead of pip
# also applicable within pipenv's shell
pipenv install request numpy
# run your script
python script.py

# add dev dependencies
pipenv install pytest --dev
# *also* install dev dependencies
pipenv install --dev

# behaves as pip, for deployment
pipenv install --system --deploy

# update dependencies
pipenv update

# generate requirements.txt for release
pipenv lock -r > requirements.txt
pipenv run pip freeze > requirements.txt
# OR
pipenv lock
pipenv install --ignore-pipfile

# show dependency graphs
pipenv graph
pipenv graph --reverse
```

### pyenv

> `nvm` for Python

[Managing Multiple Python Versions With pyenv – Real Python](https://realpython.com/intro-to-pyenv/#installing-pyenv)
[Better Python version and environment management with pyenv](http://fgimian.github.io/blog/2014/04/20/better-python-version-and-environment-management-with-pyenv/)
[pyenv/pyenv-installer: This tool is used to install `pyenv` and friends.](https://github.com/pyenv/pyenv-installer)

```sh
curl -L https://raw.github.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash
# follow the instructions
pyenv init
```

```sh
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
# this fix problems when compiling packages
PYTHON_CONFIGURE_OPTS="--enable-shared" pyenv install 3.9.5

pyenv virtualenv PROJECT
pyenv activate PROJECT
python -m pip install -r requirements.txt
pyenv deactivate

pyenv install -l
pyenv virtualenvs
pyenv versions
pyenv global VERSION
pyenv local VENV|VERSION
```

[Can't figure out how to build a python that uses the .SO file · Issue #65 · pyenv/pyenv](https://github.com/pyenv/pyenv/issues/65)
[wxPython Phoenix build fail ("Could not build python extensions"?) in pyenv 3.5.1 on Linux - wxPython Dev - Discuss wxPython](https://discuss.wxpython.org/t/wxpython-phoenix-build-fail-could-not-build-python-extensions-in-pyenv-3-5-1-on-linux/32810/13)

### virtualenv

> it is a little troublesome to setup

[Virtualenv](https://virtualenv.pypa.io/en/stable/) create python environment in local folder
[virtualenvwrapper documentation](https://virtualenvwrapper.readthedocs.io/en/latest/) create python environment in a centralized folder
[Virtualenv vs Virtualenvwrapper · Saurabh Kumar](https://saurabh-kumar.com/blog/virtualenv-vs-virtualenvwrapper.html) !important

[Code4ReferenceTutorial Python virtual environment .](http://code4reference.com/2014/05/python-virtual-environment/)
[Bob's Blog - Crafting Software: Getting Started with virtualenv and virtualenvwrapper in Python](http://www.silverwareconsulting.com/index.cfm/2012/7/24/Getting-Started-with-virtualenv-and-virtualenvwrapper-in-Python)
[Use pew, not virtualenvwrapper, for Python virtualenvs](http://planspace.org/20150120-use_pew_not_virtualenvwrapper_for_python_virtualenvs/)
[berdario/pew: A tool to manage multiple virtual environments written in pure python](https://github.com/berdario/pew)

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

## Multiple Python versions

[How to Install Python 3.7 on Ubuntu 18.04 | Linuxize](https://linuxize.com/post/how-to-install-python-3-7-on-ubuntu-18-04/)
[How to Install pip for python 3.7 on Ubuntu 18? - Stack Overflow](https://stackoverflow.com/questions/54633657/how-to-install-pip-for-python-3-7-on-ubuntu-18)

## Packages

```sh
sudo yay -S python-pipenv pyenv pyenv-virtualenv
pip install --user TermRecord ngxtop bpytop
pip install --user ipython black flake8 pyls-black
pip install --user python-pygame
```

[Python Extension Packages for Windows - Christoph Gohlke](https://www.lfd.uci.edu/~gohlke/pythonlibs/) if you have difficulties building packages
[Wheelodex — an Index of Wheels](https://www.wheelodex.org/)

[JackMcKew/awesome-python-bytes: 😎 🐍 Awesome lists about Python Bytes https://pythonbytes.fm/](https://github.com/JackMcKew/awesome-python-bytes)
[Hidden gems: 14 Python libraries too good to overlook | InfoWorld](http://www.infoworld.com/article/3164409/application-development/hidden-gems-14-python-libraries-too-good-to-overlook.html)
[6 Python libraries every programmer will love | InfoWorld](http://www.infoworld.com/article/3008915/application-development/6-python-libraries-every-programmer-will-love.html)
[4 can't-miss Python goodies from Microsoft, Google, Facebook, and Uber | InfoWorld](http://www.infoworld.com/article/3126468/application-development/4-cant-miss-python-goodies-from-microsoft-google-facebook-and-uber.html)
[Top 10 Python Libraries You Should Know | Tryolabs Blog](https://tryolabs.com/blog/2019/12/10/top-10-python-libraries-of-2019/)
[5 wicked-fast Python frameworks you have to try | InfoWorld](http://www.infoworld.com/article/3133854/application-development/5-wicked-fast-python-frameworks-you-have-to-try.html)
[The World of Zope — Zope Project and Community documentation](https://www.zope.org/world.html#tools)

[Trey Hunner](http://treyhunner.com/)
[Splinter documentation](https://splinter.readthedocs.io/en/latest/)
[Python 3 Module of the Week — PyMOTW 3](https://pymotw.com/3/)

[ActiveState/appdirs: A small Python module for determining appropriate platform-specific dirs, e.g. a "user data dir".](https://github.com/ActiveState/appdirs)

[Sending Emails With Python – Real Python](https://realpython.com/python-send-email/)

[mahmoud/boltons: 🔩 Like builtins, but boltons. Constructs/recipes/snippets that would be handy in the standard library. Nothing like Michael Bolton.](https://github.com/mahmoud/boltons)

[bwasti/cache.py: Python memoization across program runs.](https://github.com/bwasti/cache.py)

[btwael/superstring.py: A fast and memory-optimized string library for heavy-text manipulation in Python](https://github.com/btwael/superstring.py)

[ActiveState/appdirs: A small Python module for determining appropriate platform-specific dirs, e.g. a "user data dir".](https://github.com/ActiveState/appdirs)

[Notify with Python - Towards Data Science](https://towardsdatascience.com/notify-with-python-41b77d51657e)

[santinic/pampy: Pampy: The Pattern Matching for Python you always dreamed of.](https://github.com/santinic/pampy)

[Requests: HTTP for Humans™ — Requests documentation](http://docs.python-requests.org/en/master/)
[kennethreitz/requests: Python HTTP Requests for Humans™](https://github.com/kennethreitz/requests)
[Python’s Requests Library (Guide) – Real Python](https://realpython.com/python-requests/#request-headers)
[Advanced usage of Python requests - timeouts, retries, hooks](https://hodovi.ch/blog/advanced-usage-python-requests-timeouts-retries-hooks/)

Date times
[kennethreitz/maya: Datetimes for Humans™](https://github.com/kennethreitz/maya)
[kennethreitz/delegator.py: Subprocesses for Humans 2.0.](https://github.com/kennethreitz/delegator.py)
[Arrow: better dates and times for Python](http://arrow.readthedocs.io/en/latest/)
[dateutil/dateutil: Useful extensions to the standard Python datetime features](https://github.com/dateutil/dateutil)

### Web Frameworks

> see `web-development.md#wsgi`
> see `web-development.md#asgi`

[A Beginner’s Introduction to Python Web Frameworks](https://stxnext.com/blog/2018/09/27/beginners-introduction-python-frameworks)
[TypeError/secure.py: Secure 🔒 headers and cookies for Python web frameworks](https://github.com/TypeError/secure.py)

[Python Web Frameworks To Learn In 2018 | Python Frameworks | Mindfire](http://www.mindfiresolutions.com/blog/2018/03/python-web-frameworks-2018/)
[Review: 13 Python web frameworks compared | InfoWorld](https://www.infoworld.com/article/3105502/python/review-13-python-web-frameworks-compared.html)

[A familiar HTTP Service Framework — responder 1.1.3 documentation](https://python-responder.org/en/latest/)

#### Flask

[Welcome | Flask (A Python Microframework)](http://flask.pocoo.org/)
[humiaozuzu/awesome-flask: A curated list of awesome Flask resources and plugins](https://github.com/humiaozuzu/awesome-flask)

[Flask Apps - Open-Source Web Apps built with automation tools - DEV Community 👩‍💻👨‍💻](https://dev.to/sm0ke/flask-apps-open-source-web-apps-built-with-automation-tools-10dh)

[Extensions Registry | Flask (A Python Microframework)](http://flask.pocoo.org/extensions/)
[Flask-RESTPlus documentation](https://flask-restplus.readthedocs.io/en/stable/)

[Python Flask From Scratch - YouTube](https://www.youtube.com/playlist?list=PLillGF-RfqbbbPz6GSEM9hLQObuQjNoj_)
[Miguel Grinberg - Flask Workshop - PyCon 2015 - YouTube](https://www.youtube.com/watch?v=DIcpEg77gdE)
[Miguel Grinberg - Flask at Scale - PyCon 2016 - YouTube](https://www.youtube.com/watch?v=tdIIJuPh3SI)
[miguelgrinberg/flack: Companion code to my PyCon 2016 "Flask at Scale" tutorial session.](https://github.com/miguelgrinberg/flack)
[Miguel Grinberg - Microservices with Python and Flask - PyCon 2017 - YouTube](https://www.youtube.com/watch?v=nrzLdMWTRMM)
[BUILDING MICROSERVICES WITH PYTHON AND FLASK - YouTube](https://www.youtube.com/watch?v=1X3_gQwfabI)
[Flask web development with Python - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDcOS4l8RCWh0olq_je0OKaP)
[Practical Flask Web Development Tutorials - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDc_owjTbIY4rbgXOFkUYOUB)

[Flask project setup: TDD, Docker, Postgres and more - Part 1 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/07/05/flask-project-setup-tdd-docker-postgres-and-more-part-1/)
[Flask project setup: TDD, Docker, Postgres and more - Part 2 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/07/06/flask-project-setup-tdd-docker-postgres-and-more-part-2/)
[Flask project setup: TDD, Docker, Postgres and more - Part 3 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/07/07/flask-project-setup-tdd-docker-postgres-and-more-part-3/)

[Flask Tutorials – Real Python](https://realpython.com/tutorials/flask/)
[Python REST APIs With Flask, Connexion, and SQLAlchemy – Real Python](https://realpython.com/flask-connexion-rest-api/)
[Python REST APIs With Flask, Connexion, and SQLAlchemy – Part 2 – Real Python](https://realpython.com/flask-connexion-rest-api-part-2/)
[Python REST APIs With Flask, Connexion, and SQLAlchemy – Part 3 – Real Python](https://realpython.com/flask-connexion-rest-api-part-3/)
[Python REST APIs With Flask, Connexion, and SQLAlchemy – Part 4 – Real Python](https://realpython.com/flask-connexion-rest-api-part-4/)

[Creating REST Services With Flask - DZone Integration](https://dzone.com/articles/creating-rest-services-with-flask)
[Get started writing your own web services using Python Flask | Opensource.com](https://opensource.com/article/17/3/writing-web-service-using-python-flask)
[peterrus/flask-docker-debugging-vscode-example: Dockerized Flask Development Workflow in VSCode Example](https://github.com/peterrus/flask-docker-debugging-vscode-example)

```
flask-RESTful flask-restless
flask-security flask-sqlalchemy
```

[Category: Flask - miguelgrinberg.com](https://blog.miguelgrinberg.com/category/Flask)
[How Secure Is The Flask User Session? - miguelgrinberg.com](https://blog.miguelgrinberg.com/post/how-secure-is-the-flask-user-session)
["Flask At Scale" tutorial at PyCon 2016 in Portland - miguelgrinberg.com](https://blog.miguelgrinberg.com/post/flask-at-scale-tutorial-at-pycon-2016-in-portland)
[The Flask Mega-Tutorial, Part I: Hello, World! - miguelgrinberg.com](http://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)
[Running Your Flask Application Over HTTPS - miguelgrinberg.com](https://blog.miguelgrinberg.com/post/running-your-flask-application-over-https)
[Migrating from Flask-Script to the New Flask CLI - miguelgrinberg.com](https://blog.miguelgrinberg.com/post/migrating-from-flask-script-to-the-new-flask-cli)

[Build a CRUD Web App With Python and Flask – Part Two | Scotch](https://scotch.io/tutorials/build-a-crud-web-app-with-python-and-flask-part-two)
[Build a CRUD Web App With Python and Flask – Part Two | Scotch](https://scotch.io/tutorials/build-a-crud-web-app-with-python-and-flask-part-two)
[Build a CRUD Web App With Python and Flask – Part Three | Scotch](https://scotch.io/tutorials/build-a-crud-web-app-with-python-and-flask-part-three)

#### Masonite

[Introduction - Masonite Documentation](https://docs.masoniteproject.com/)
[MasoniteFramework/masonite: The Modern And Developer Centric Python Web Framework](https://github.com/MasoniteFramework/masonite)
[Masonite Framework Tutorial Series Part 1 - Installation - DEV Community 👩‍💻👨‍💻](https://dev.to/josephmancuso/masonite-framework-tutorial-series-part-1-140e)
[Masonite Framework Tutorial Series Part 2 - Routing - DEV Community 👩‍💻👨‍💻](https://dev.to/josephmancuso/masonite-framework-tutorial-series-part-2---routing-1ak3)

[Masonite Python Framework - New Dashboard Package! - DEV Community 👩‍💻👨‍💻](https://dev.to/josephmancuso/masonite-python-framework---new-dashboard-package-31hb)

#### Async

> see `web-development.md#ASGI`

[FastAPI](https://fastapi.tiangolo.com/)
[tiangolo/fastapi: FastAPI framework, high performance, easy to learn, fast to code, ready for production](https://github.com/tiangolo/fastapi) Starlette + Pydantic + OpenAPI doc
[FastAPI Course for Beginners - YouTube](https://www.youtube.com/watch?v=tLKKmouUams)
[FastAPI Course – Code APIs Quickly](https://www.freecodecamp.org/news/fastapi-helps-you-develop-apis-quickly/)

[Starlette](https://www.starlette.io/)

[Falcon | The minimal, fast, and secure web framework for Python](https://falconframework.org/)

[pgjones / quart · GitLab](https://gitlab.com/pgjones/quart)

#### Django

> see `django.md`

#### Pyramid

[Welcome to Pyramid, a Python Web Framework](https://trypyramid.com/)
[Pyramid Community Cookbook](https://docs.pylonsproject.org/projects/pyramid-cookbook/en/latest/index.html)

[Welcome to the Pylons Project](https://pylonsproject.org/) Pyramid is part of Pylons project
[Pylons Reference Documentation — Pylons Framework documentation](https://docs.pylonsproject.org/projects/pylons-webframework/en/latest/)

#### Honorable Mentions

[Bottle: Python Web Framework — Bottle 0.13-dev documentation](http://bottlepy.org/docs/dev/)
[bottlepy/bottle: bottle.py is a fast and simple micro-framework for python web-applications.](https://github.com/bottlepy/bottle)

[CherryPy — A Minimalist Python Web Framework](https://cherrypy.org/)
[cherrypy/cherrypy: CherryPy is a pythonic, object-oriented HTTP framework. https://docs.cherrypy.org/](https://github.com/cherrypy/cherrypy)

[Tornado Web Server — Tornado documentation](http://www.tornadoweb.org/en/stable/)
\
[www.web2py.com](http://www.web2py.com/)
[web2py - Preface](http://web2py.com/book) the manual
[Welcome to web2py’s API documentation!](http://web2py.readthedocs.io/en/latest/)
[web2py video course 2013 on Vimeo](https://vimeo.com/album/3016728)

[jczic/MicroWebSrv: A micro HTTP Web server that supports WebSockets, html/python language templating and routing handlers, for MicroPython (used on Pycom modules & ESP32)](https://github.com/jczic/MicroWebSrv)
[channelcat/sanic: Async Python 3.5+ web server that's written to go fast](https://github.com/channelcat/sanic)
[encode/apistar: A smart Web API framework, designed for Python 3. 🌟](https://github.com/encode/apistar)
[molten: modern API framework — molten 0.1.0 documentation](https://moltenframework.com/)

### Testing

[Top 5 Python Frameworks For Test Automation In 2019 | LambdaTest](https://www.lambdatest.com/blog/top-5-python-frameworks-for-test-automation-in-2019/)

[Getting Started With Testing in Python – Real Python](https://realpython.com/python-testing/)
[Effective Python Testing With Pytest – Real Python](https://realpython.com/pytest-python-testing/)
[Continuous Integration With Python: An Introduction – Real Python](https://realpython.com/python-continuous-integration/)
[wily · PyPI](https://pypi.org/project/wily/)
[Testing Your Code — The Hitchhiker's Guide to Python](https://docs.python-guide.org/writing/tests/)
[An Introduction to Unit Testing in Python](https://www.freecodecamp.org/news/an-introduction-to-testing-in-python/)

[unittest — Unit testing framework — Python documentation](https://docs.python.org/3/library/unittest.html)
[Improve Your Tests With the Python Mock Object Library – Real Python](https://realpython.com/courses/python-mock-object-library/) `unittest.mock`

[Welcome to the tox automation project — tox documentation](https://tox.readthedocs.io/en/latest/)

[Your way out of The Lack of Testing Death Spiral - Pythoscope](http://pythoscope.wikidot.com/)
[mkwiatkowski/pythoscope: unit test generator for Python](https://github.com/mkwiatkowski/pythoscope)

[Refactoring with tests in Python: a practical example - The Digital Cat](https://www.thedigitalcatonline.com/blog/2017/07/21/refactoring-with-test-in-python-a-practical-example/)
[TDD in Python with pytest - YouTube](https://www.youtube.com/playlist?list=PLWtCrYLGt7T2REIrEcpGY6nT2t7Wcoj-m)
[TDD in Python with pytest - Part 1 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/09/10/tdd-in-python-with-pytest-part-1/)
[TDD in Python with pytest - Part 2 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/09/11/tdd-in-python-with-pytest-part-2/)
[TDD in Python with pytest - Part 3 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/09/15/tdd-in-python-with-pytest-part-3/)
[TDD in Python with pytest - Part 4 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/09/17/tdd-in-python-with-pytest-part-4/)
[TDD in Python with pytest - Part 5 - The Digital Cat](https://www.thedigitalcatonline.com/blog/2020/09/21/tdd-in-python-with-pytest-part-5/)

### Logging

[16.6. logging — Logging facility for Python — Python documentation](https://docs.python.org/3/library/logging.html)
[Logging HOWTO — Python documentation](https://docs.python.org/3/howto/logging.html)
[Logging Cookbook — Python documentation](https://docs.python.org/3/howto/logging-cookbook.html)
[A guide to logging in Python | Opensource.com](https://opensource.com/article/17/9/python-logging)
[Python Logging: In-Depth Tutorial | Toptal](https://www.toptal.com/python/in-depth-python-logging)
[Logging in Python ~ The Python Corner](https://www.thepythoncorner.com/2018/05/logging-in-python.html)
[Logging — The Hitchhiker's Guide to Python](https://docs.python-guide.org/writing/logging/)

[Logging in Python – Real Python](https://realpython.com/python-logging/)
[Python Logging: A Stroll Through the Source Code – Real Python](https://realpython.com/python-logging-source-code/)
[How to Collect, Customize, and Centralize Python Logs | Datadog](https://www.datadoghq.com/blog/python-logging-best-practices/)

[Python logging and rotating files - Stack Overflow](https://stackoverflow.com/questions/9106795/python-logging-and-rotating-files/20755477)
[logging - How to create rolling logger in Python - Stack Overflow](https://stackoverflow.com/questions/56195040/how-to-create-rolling-logger-in-python)

[python - logger configuration to log to file and print to stdout - Stack Overflow](https://stackoverflow.com/questions/13733552/logger-configuration-to-log-to-file-and-print-to-stdout/13733863#13733863)
[acschaefer/duallog: Python package to enable simultaneous logging to console and logfile.](https://github.com/acschaefer/duallog)

```python
def logger_setup(
    filename=None, when="d", interval=1, backup_count=21, level=logging.INFO
):
    formatter = logging.Formatter(
        "%(asctime)s - %(name)s - %(levelname)s - %(message)s"
    )
    # formatter.converter = time.gmtime  # if you want UTC time
    root_logger = logging.getLogger()
    root_logger.setLevel(level)

    if filename is not None:
        file_handler = logging.handlers.TimedRotatingFileHandler(
            filename=filename,
            when=when,
            interval=interval,
            backupCount=backup_count,
        )
        file_handler.setFormatter(formatter)
        root_logger.addHandler(file_handler)

    console_handler = logging.StreamHandler(sys.stdout)
    console_handler.setFormatter(formatter)
    root_logger.addHandler(console_handler)
```

[Python's Built-In 'logging' Module - YouTube](https://www.youtube.com/watch?v=4t67SNWoPxk)

[Geal/nom: Rust parser combinator framework](https://github.com/Geal/nom)
[kopensource/colored_logs](https://github.com/kopensource/colored_logs)

[gruns/icecream: 🍦 Never use print() to debug again.](https://github.com/gruns/icecream)
[Stop Using Print to Debug in Python. Use Icecream Instead | by Khuyen Tran | Towards Data Science](https://towardsdatascience.com/stop-using-print-to-debug-in-python-use-icecream-instead-79e17b963fcc)
[Do Not Use Print For Debugging In Python Anymore | by Christopher Tao | Jun, 2021 | Towards Data Science](https://towardsdatascience.com/do-not-use-print-for-debugging-in-python-anymore-6767b6f1866d)

[Do not log](https://sobolevn.me/2020/03/do-not-log)

### Async I/O

[timofurrer/awesome-asyncio: A curated list of awesome Python asyncio frameworks, libraries, software and resources](https://github.com/timofurrer/awesome-asyncio)

[Comparing gevent to eventlet | Concurrency in Python](https://blog.gevent.org/2010/02/27/why-gevent/)
[What is gevent? — gevent documentation](http://www.gevent.org/) uses libev

[Eventlet Networking Library](http://eventlet.net/)

[MagicStack/uvloop: Ultra fast asyncio event loop.](https://github.com/MagicStack/uvloop) uses uvloop

[python - How does asyncio actually work? - Stack Overflow](https://stackoverflow.com/questions/49005651/how-does-asyncio-actually-work)
[Asynchronous I/O With Python 3](https://code.tutsplus.com/tutorials/asynchronous-io-with-python-3--cms-29045)
[Async IO in Python: A Complete Walkthrough – Real Python](https://realpython.com/async-io-python/)
[Asyncio : A tutorial for the beginners | KnowPapa](https://knowpapa.com/asyncio/)
[Hands-on Python 3 Concurrency With the asyncio Module – Real Python](https://realpython.com/courses/python-3-concurrency-asyncio-module/)
[Asynchronous Programming in Python | Asyncio (Guide)](https://djangostars.com/blog/asynchronous-programming-in-python-asyncio/)
[How to use asyncio in Python | InfoWorld](https://www.infoworld.com/article/3526429/how-to-use-asyncio-in-python.html)
[3 steps to a Python async overhaul | InfoWorld](https://www.infoworld.com/article/3562577/3-steps-to-a-python-async-overhaul.html)
[Python async/await Tutorial](https://stackabuse.com/python-async-await-tutorial)

[Coroutines and Tasks — Python documentation](https://docs.python.org/3/library/asyncio-task.html)
[asyncio — Asynchronous I/O — Python documentation](https://docs.python.org/3/library/asyncio.html)
[asyncio — Asynchronous I/O, event loop, and concurrency tools — PyMOTW 3](https://pymotw.com/3/asyncio/)
[pymotw3/source/asyncio at master · reingart/pymotw3](https://github.com/reingart/pymotw3/tree/master/source/asyncio)
[Asyncio Documentation — Asyncio Documentation documentation](http://asyncio.readthedocs.io/en/latest/index.html)

[aio-libs](https://github.com/aio-libs)
[Tinche/aiofiles: File support for asyncio](https://github.com/Tinche/aiofiles)
[theelous3/asks: Async requests-like httplib for python.](https://github.com/theelous3/asks)
[vxgmichel/aiostream: Generator-based operators for asynchronous iteration](https://github.com/vxgmichel/aiostream)

[Welcome to AIOHTTP — aiohttp documentation](https://aiohttp.readthedocs.io/en/stable/)

[Unsync](http://asherman.io/projects/unsync.html) ambient event loop
[alex-sherman/unsync: Unsynchronize asyncio](https://github.com/alex-sherman/unsync)

#### Curio

[Curio documentation](https://curio.readthedocs.io/en/latest/) coroutine-based library for concurrent Python systems programming
[A Tutorial Introduction — Curio documentation](https://curio.readthedocs.io/en/latest/tutorial.html)
[dabeaz/curio: Get that harness ready and hold on tight--Curio is gonna take YOU for a walk.](https://github.com/dabeaz/curio)

[#107: Python concurrency with Curio - YouTube](https://www.youtube.com/watch?v=cetvzYugGIc)

### Trio

[Trio: a friendly Python library for async concurrency and I/O](https://trio.readthedocs.io/en/latest/index.html)
[python-trio/trio: Trio – a friendly Python library for async concurrency and I/O](https://github.com/python-trio/trio)

[python - What is the core difference between asyncio and trio? - Stack Overflow](https://stackoverflow.com/questions/49482969/what-is-the-core-difference-between-asyncio-and-trio)

### Socket programming

[socket — Low-level networking interface — Python documentation](https://docs.python.org/3/library/socket.html)
[socketserver — A framework for network servers — Python documentation](https://docs.python.org/3/library/socketserver.html)

[Socket Programming in Python (Guide) – Real Python](https://realpython.com/python-sockets/)

### Distributed Computing

[6 Python libraries for parallel processing | InfoWorld](https://www.infoworld.com/article/3542595/6-python-libraries-for-parallel-processing.html)

[execnet: Distributed Python deployment and communication](http://codespeak.net/execnet/)

[Homepage | Celery: Distributed Task Queue](http://www.celeryproject.org/)

[rq/rq: Simple job queues for Python](https://github.com/rq/rq)
[RQ: Simple job queues for Python](https://python-rq.org/)
[Introducing RQ » nvie.com](https://nvie.com/posts/introducing-rq/)

[closeio/tasktiger: Python task queue. Because celery is gross.](https://github.com/closeio/tasktiger)

[Welcome to PyPubSub’s Home Page! — Pypubsub v4.0.3 Documentation](https://pypubsub.readthedocs.io/en/v4.0.3/)
[schollii/pypubsub: A Python publish-subcribe library (moved here from SourceForge.net where I had it for many years)](https://github.com/schollii/pypubsub)

### Image manipulation

[Wand documentation](http://docs.wand-py.org/en/latest/index.html#)
[ImageMagick/PythonMagick: PythonMagick](https://github.com/ImageMagick/PythonMagick)
[python - Documents and examples of PythonMagick - Stack Overflow](http://stackoverflow.com/questions/1740158/documents-and-examples-of-pythonmagick/5188661#5188661)

[Python Imaging Library (PIL)](http://www.pythonware.com/products/pil/)
[Pillow — Pillow (PIL Fork) documentation](http://pillow.readthedocs.io/en/latest/)
`python-image` of most distro points to `pillow`
[Image Module — Pillow (PIL Fork) documentation](https://pillow.readthedocs.io/en/stable/reference/Image.html)
[Concepts — Pillow (PIL Fork) documentation](https://pillow.readthedocs.io/en/stable/handbook/concepts.html)

[Imageio website](https://imageio.github.io/)

### Configs

[python-decouple · PyPI](https://pypi.org/project/python-decouple/) load `.env`
[Do You Really Need Environment Variables in Python? | iRead](https://iread.ga/posts/49/do-you-really-need-environment-variables-in-python)

#### ConfigParser

[configparser — Configuration file parser — Python documentation](https://docs.python.org/3/library/configparser.html)

```python
import configparser

config = configparser.ConfigParser()
config.read(config_path)
print({section: dict(config[section]) for section in config.sections()})
```

### Database/ORM

[Object-relational Mappers (ORMs) - Full Stack Python](https://www.fullstackpython.com/object-relational-mappers-orms.html)
[Why should you use an ORM (Object Relational Mapper)? - HedgeDoc](https://monadical.com/posts/why-use-orm.html)

[SQLAlchemy - The Database Toolkit for Python](http://www.sqlalchemy.org/)
[dahlia/awesome-sqlalchemy: A curated list of awesome tools for SQLAlchemy](https://github.com/dahlia/awesome-sqlalchemy)
[Data Management With Python, SQLite, and SQLAlchemy – Real Python](https://realpython.com/python-sqlite-sqlalchemy/)
[How to fix common pitfalls with the Python ORM tool SQLAlchemy | Opensource.com](https://opensource.com/article/19/9/common-pitfalls-python)
[SQLAlchemy ORM — a more “Pythonic” way of interacting with your database](https://medium.com/dataexplorations/sqlalchemy-orm-a-more-pythonic-way-of-interacting-with-your-database-935b57fd2d4d)

[coleifer/peewee: a small, expressive orm -- supports postgresql, mysql and sqlite](https://github.com/coleifer/peewee)
[Peewee Tutorial - Tutorialspoint](https://www.tutorialspoint.com/peewee/index.htm)

[kennethreitz/records: SQL for Humans™](https://github.com/kennethreitz/records)
[MagicStack/asyncpg: A fast PostgreSQL Database Client Library for Python/asyncio.](https://github.com/MagicStack/asyncpg)

### CLI

[prompt-toolkit](https://github.com/prompt-toolkit?type=source)

[MasterOdin/crayons: Text UI colors for Python.](https://github.com/MasterOdin/crayons)
[tartley/colorama: Simple cross-platform colored terminal text in Python](https://github.com/tartley/colorama)

[tabulate · PyPI](https://pypi.org/project/tabulate/) pretty print table and dict

[Pytabby: a tabbed menu system for console-based Python programs - DEV Community 👩‍💻👨‍💻](https://dev.to/prooffreader/pytabby-a-tabbed-menu-system-for-console-based-python-programs-301n)

[tqdm documentation](https://tqdm.github.io/)
[tqdm/tqdm: A fast, extensible progress bar for Python and CLI](https://github.com/tqdm/tqdm)

[Overview — Urwid](http://urwid.org/)
[urwid/urwid: Console user interface library for Python (official repo)](https://github.com/urwid/urwid)

[amoffat/sh: Python process launching](https://github.com/amoffat/sh)

#### Prompt

[prompt-toolkit/python-prompt-toolkit: Library for building powerful interactive command line applications in Python](https://github.com/prompt-toolkit/python-prompt-toolkit)
[python-cmd2/cmd2: cmd2 - quickly build feature-rich and user-friendly interactive command line applications in Python](https://github.com/python-cmd2/cmd2)

[willmcgugan/textual: Textual is a TUI (Text User Interface) framework for Python inspired by modern web development.](https://github.com/willmcgugan/textual)
[willmcgugan/rich: Rich is a Python library for rich text and beautiful formatting in the terminal.](https://github.com/willmcgugan/rich)
[Welcome to Rich’s documentation!](https://rich.readthedocs.io/en/latest/)

[Introducing Textual](https://www.willmcgugan.com/blog/tech/post/textual-progress/) uses Rich internally
[Building Rich terminal dashboards](https://www.willmcgugan.com/blog/tech/post/building-rich-terminal-dashboards/)
[Rendering a tree view in the terminal with Python and Rich](https://www.willmcgugan.com/blog/tech/post/rich-tree/)

#### Parser

[Comparing Python Command-Line Parsing Libraries - Argparse, Docopt, and Click - Real Python](https://realpython.com/comparing-python-command-line-parsing-libraries-argparse-docopt-click/)
[Building Beautiful Command Line Interfaces with Python | by Oyetoke Tobi Emmanuel | codeburst](https://codeburst.io/building-beautiful-command-line-interfaces-with-python-26c7e1bb54df)

[chriskiehl/Gooey: Turn (almost) any Python command line program into a full GUI application with one line](https://github.com/chriskiehl/Gooey)

[argparse — Parser for command-line options, arguments and sub-commands — Python documentation](https://docs.python.org/3/library/argparse.html)
[Python Argparse Cookbook - mkaz.tech](https://mkaz.tech/code/python-argparse-cookbook.html)
[PEP 389 -- argparse - New Command Line Parsing Module | Python.org](https://www.python.org/dev/peps/pep-0389/)
[Python Argparse Cookbook – mkaz.blog](https://mkaz.blog/code/python-argparse-cookbook/)
[Learn Enough Python to be Useful: argparse – Towards Data Science](https://towardsdatascience.com/learn-enough-python-to-be-useful-argparse-e482e1764e05)
[How to Master Python Command Line Arguments - Towards Data Science](https://towardsdatascience.com/how-to-master-python-command-line-arguments-5d5ad4bcf985)

[Welcome to Click — Click Documentation](https://click.palletsprojects.com/)
[Writing Python Command-Line Tools With Click – dbader.org](https://dbader.org/blog/python-commandline-tools-with-click)
[Mastering Click: Writing Advanced Python Command-Line Apps – dbader.org](https://dbader.org/blog/mastering-click-advanced-python-command-line-apps)
[Super Easy Python CLI with Click | CODING w/RICKY](http://www.codingwithricky.com/2019/08/18/easy-python-cli-with-click/)
[How to Write Python Command-Line Interfaces like a Pro](https://towardsdatascience.com/how-to-write-python-command-line-interfaces-like-a-pro-f782450caf0d)
[click-contrib](https://github.com/click-contrib)

[cliff – Command Line Interface Formulation Framework — cliff documentation](https://docs.openstack.org/cliff/latest/)

[Argh: The Natural CLI — argh documentation](https://pythonhosted.org/argh/)

[mando - CLI interfaces for Humans — mando documentation](https://mando.readthedocs.io/en/latest/)
[rubik/mando: Create Python CLI apps with little to no effort at all!](https://github.com/rubik/mando)

[kbknapp/Clapp-py: A small library for quickly and easily creating command line applications in python.](https://github.com/kbknapp/Clapp-py)

[docopt—language for description of command-line interfaces](http://docopt.org/)
[Python argparse: Make at least one argument required - Stack Overflow](https://stackoverflow.com/questions/6722936/python-argparse-make-at-least-one-argument-required) docopt example

#### Framework

[Typer](https://typer.tiangolo.com/) FastAPI's CLI sibling, uses Click
[tiangolo/typer: Typer, build great CLIs. Easy to code. Based on Python type hints.](https://github.com/tiangolo/typer)

[Cement Framework](https://builtoncement.com/)
[timsavage/pyapp: A Python Application framework - Let us handle the boring stuff!](https://github.com/timsavage/pyapp)

[google/python-fire: Python Fire is a library for automatically generating command line interfaces (CLIs) from absolutely any Python object.](https://github.com/google/python-fire)

### Project Generators

[Cookiecutter: Better Project Templates — cookiecutter documentation](http://cookiecutter.readthedocs.io/en/latest/)
[cookiecutter/cookiecutter: A command-line utility that creates projects from cookiecutters (project templates), e.g. Python package projects, VueJS projects.](https://github.com/cookiecutter/cookiecutter)

[Raphael Pierzina - Kickstarting projects with Cookiecutter - YouTube](https://www.youtube.com/watch?v=nExL0SgKsDY)

[Cookiecutter Templates](http://cookiecutter-templates.sebastianruml.name/)
[nvie/cookiecutter-python-cli](https://github.com/nvie/cookiecutter-python-cli)

[bpw1621/ordained: An opinionated template for Python packages.](https://github.com/bpw1621/ordained)
[ORDAINED: The Python Project Template - KDnuggets](https://www.kdnuggets.com/2021/11/ordained-python-project-template.html)

### GUI

> see `qt.md#python`
> see `cross-platform-apps-desktop.md`

### eBook

[Overview — Sphinx documentation](http://www.sphinx-doc.org/en/stable/)
[aerkalov/ebooklib: Python E-book library for handling books in EPUB2/EPUB3 and Kindle format -](https://github.com/aerkalov/ebooklib/)
[anqxyr/mkepub: Simple minimalistic library for creating EPUB3 files](https://github.com/anqxyr/mkepub)

### SimPy

[Overview — SimPy documentation](https://simpy.readthedocs.io/en/latest/index.html) Discrete event simulation for Python
[SimPY - YouTube](https://www.youtube.com/playlist?list=PL2Wg3oyN-jmMD39JFqejZAzi06BWo_uJa)
[Meghan Heintz: Launching a new warehouse with SimPy at Rent the Runway | PyData New York City 2019 - YouTube](https://www.youtube.com/watch?v=693UiPq6mII)
[Basics of Discrete Event Simulation using SimPy in Python](https://www.tutorialspoint.com/basics-of-discrete-event-simulation-using-simpy-in-python)

### Hydra

[Hydra | Hydra](https://hydra.cc/)
[Open-sourcing Hydra for simpler app development - Facebook Engineering](https://engineering.fb.com/open-source/hydra/)

[Hydra — A fresh look at configuration for machine learning projects | by PyTorch | PyTorch | Medium](https://medium.com/pytorch/hydra-a-fresh-look-at-configuration-for-machine-learning-projects-50583186b710)

[FLOSS Weekly 573 Hydra](https://twit.tv/shows/floss-weekly/episodes/573)

## Modules

Module corresponds to files, package corresponds to folder.

[6. Modules — Python documentation](https://docs.python.org/3/tutorial/modules.html)
[Python Modules: Creating, Importing, and Sharing](http://stackabuse.com/python-modules-creating-importing-and-sharing/)
[Python Circular Imports](http://stackabuse.com/python-circular-imports/)
[site — Site-specific configuration hook — Python documentation](https://docs.python.org/3/library/site.html)

[Python Modules and Packages – An Introduction – Real Python](https://realpython.com/python-modules-packages/)
[Python import: Advanced Techniques and Tips – Real Python](https://realpython.com/python-import/)
[The Module Search Path – Real Python](https://realpython.com/lessons/module-search-path/)
[Python behind the scenes #11: how the Python import system works](https://tenthousandmeters.com/blog/python-behind-the-scenes-11-how-the-python-import-system-works/)

Module search path:

- current directory
- environment variable [PYTHONPATH](https://docs.python.org/3/using/cmdline.html#envvar-PYTHONPATH)
- installation dependent list of directories

The resulting search path is accessible in the Python variable `sys.path` which you can manipulate

[PEP 420 -- Implicit Namespace Packages | Python.org](https://www.python.org/dev/peps/pep-0420/)
`__init__.py` be required, not anymore since 3.3
`import *` will load `__all__: list[str]` from `__init__.py` (package) or module

[Python Zip Imports: Distribute Modules and Packages Quickly – Real Python](https://realpython.com/preview/python-zip-import/)
[Live-reloading of Python Modules in the Python REPL / IPython / Jupyter Console - DEV Community 👩‍💻👨‍💻](https://dev.to/preslavrachev/live-reloading-of-python-modules-in-the-python-repl--ipython--jupyter-console-1d17)

### `importlib`

[Writing a Domain Specific Language (DSL) in Python – dbader.org](https://dbader.org/blog/writing-a-dsl-with-python)

### packaging

[Python Packaging User Guide — Python Packaging User Guide](https://packaging.python.org/)
[Packaging Python Projects — Python Packaging User Guide](https://packaging.python.org/tutorials/packaging-projects/)
[Packaging and Distributing Projects — Python Packaging User Guide](https://packaging.python.org/tutorials/distributing-packages/)
[Packaging and distributing projects — Python Packaging User Guide](https://packaging.python.org/guides/distributing-packages-using-setuptools/)

[How to Create a Python Package - Python Central](https://www.pythoncentral.io/how-to-create-a-python-package/)
[How To Package Your Python Code — Python Packaging Tutorial](https://python-packaging.readthedocs.io/en/latest/index.html)
[The Sheer Joy of Packaging! — The Joy of Packaging documentation](https://python-packaging-tutorial.readthedocs.io/en/latest/index.html)
[A tutorial on packaging up your Python code for PyPI](https://snarky.ca/a-tutorial-on-python-package-building/)
[Building a Python API for Raspberry Pi hardware - Speaker Deck](https://speakerdeck.com/bennuttall/building-a-python-api-for-raspberry-pi-hardware)
[Packaging a python library | ionel's codelog](https://blog.ionelmc.ro/2014/05/25/python-packaging/)
[A tutorial on packaging up your Python code for PyPI](https://snarky.ca/a-tutorial-on-python-package-building/)
["Publishing well-formed Python packages" - Julin S (PyConline AU 2020) - YouTube](https://www.youtube.com/watch?v=_b8D4v7YIME)

[Welcome to Setuptools’ documentation! — setuptools documentation](https://setuptools.readthedocs.io/en/latest/)
[Python Entry Points Explained](https://amir.rachum.com/blog/2017/07/28/python-entry-points/)

[How to use GitHub as a PyPi server – freeCodeCamp.org](https://medium.freecodecamp.org/how-to-use-github-as-a-pypi-server-1c3b0d07db2)

`distutil` is [deprecated](https://pypi.org/project/Distutils2/) by `setuptools`

[OpenStack Docs: `pbr` Usage](https://docs.openstack.org/pbr/latest/user/using.html)
Build wheel with a minimal `setup.py` and `setup.cfg`.
[Building a Python package, and a docker image via Pipenv](https://medium.com/@greut/building-a-python-package-a-docker-image-using-pipenv-233d8793b6cc)

```sh
python setup.py bdist_wheel
```

[The difference between setup.py (pyproject.toml) and requirements.txt (Pipfile) · Issue #27 · pypa/pipfile](https://github.com/pypa/pipfile/issues/27)
[setup.py vs requirements.txt · caremad](https://caremad.io/posts/2013/07/setup-vs-requirement/)
[Pipfile vs setup.py — pipenv documentation](https://docs.pipenv.org/advanced/#pipfile-vs-setuppy)

[The Many Layers of Packaging — Sedimental](https://sedimental.org/the_packaging_gradient.html)
[Mahmoud Hashemi, "The Packaging Gradient", PyBay2017 - YouTube](https://www.youtube.com/watch?v=iLVNWfPWAC8) [slide](https://speakerdeck.com/mhashemi/the-packaging-gradient)
[An Introduction to Python Packages for Absolute Beginners - By Ramit Mittal](https://hackernoon.com/pip-install-abra-cadabra-or-python-packages-for-beginners-33a989834975)

[Pipenv: A Guide to the New Python Packaging Tool – Real Python](https://realpython.com/pipenv-guide/#package-distribution) Using `setuptools` with `pipenv`
Put dependencies in `setup.py` instead of `Pipfile`, use `pipenv install -e` to install package locally.

[Publishing your own Python package - Towards Data Science](https://towardsdatascience.com/publishing-your-own-python-package-3762f0d268ec) !important

[pypa/sampleproject: A sample project that exists for PyPUG's "Tutorial on Packaging and Distributing Projects"](https://github.com/pypa/sampleproject)
[requests/setup.py at master · requests/requests](https://github.com/requests/requests/blob/master/setup.py) `setuptools`
[numpy/setup.py at master · numpy/numpy](https://github.com/numpy/numpy/blob/master/setup.py) `distutils`?

[ofek/hatch: A modern project, package, and virtual env manager for Python](https://github.com/ofek/hatch) build, test and upload with one CLI

[Welcome to twine’s documentation! — twine documentation](https://twine.readthedocs.io/en/latest/) THE recommended tool
[pypa/twine: Utilities for interacting with PyPI](https://github.com/pypa/twine) publishing

[pypa/wheel: The official binary distribution format for Python](https://github.com/pypa/wheel)
[pypa/manylinux: Python wheels that work on any linux (almost)](https://github.com/pypa/manylinux)
[pypa/python-manylinux-demo: Demo project for building Python wheels for Linux with Travis-CI](https://github.com/pypa/python-manylinux-demo)

[bump2version · PyPI](https://pypi.org/project/bump2version/) Version-bump your software with a single command!

### `pyproject.toml`

Defines `pyproject.toml`, replaces `setuptools` and `setup.py`.
[PEP 518 -- Specifying Minimum Build System Requirements for Python Projects | Python.org](https://www.python.org/dev/peps/pep-0518/)
[PEP 517 -- A build-system independent format for source trees | Python.org](https://www.python.org/dev/peps/pep-0517/)
[Dependency specification in pyproject.toml based on PEP 508 | Python.org](https://www.python.org/dev/peps/pep-0631/)

[Clarifying PEP 518 (a.k.a. pyproject.toml)](https://snarky.ca/clarifying-pep-518/)
[What the heck is pyproject.toml?](https://snarky.ca/what-the-heck-is-pyproject-toml/)

[takluyver/flit: Simplified packaging of Python modules](https://github.com/takluyver/flit)
[Flit 1.0 — Flit documentation](https://flit.readthedocs.io/en/latest/) build with `pyproject.toml`

[David-OConnor/pyflow: An installation and dependency system for Python](https://github.com/David-OConnor/pyflow)

> see `#poetry`

### PyBuilder

[PyBuilder — Usage Documentation](https://pybuilder.io/documentation/manual)

## Freezing

The act of bundling all dependencies, and optionally to make a standalone binary, is called _freezing_ in Python

[Packaging Archives - The Mouse Vs. The Python](http://www.blog.pythonlibrary.org/category/packaging/)
[Episode #245 Python packaging landscape in 2020 - [Talk Python To Me Podcast]](https://talkpython.fm/episodes/show/245/python-packaging-landscape-in-2020)
[tryexceptpass - 4 Attempts at Packaging Python as an Executable](https://tryexceptpass.org/article/package-python-as-executable/)

[schmir/bbfreeze: UNMAINTAINED](https://github.com/schmir/bbfreeze)
[A bbfreeze Tutorial – Build a Binary Series! | The Mouse Vs. The Python](https://www.blog.pythonlibrary.org/2010/08/19/a-bbfreeze-tutorial-build-a-binary-series/)

[`py2exe`](http://www.py2exe.org/) and [`py2app`](https://wiki.python.org/moin/MacPython/py2app) are Windows and OSX specific solution

[Nuitka Home | Nuitka Home](http://nuitka.net/)

[Briefcase](https://briefcase.readthedocs.io/en/latest/)

[linkedin/shiv: shiv is a command line utility for building fully self contained Python zipapps as outlined in PEP 441, but with all their dependencies included.](https://github.com/linkedin/shiv)

[pantsbuild/pex: A library and tool for generating .pex (Python EXecutable) files](https://github.com/pantsbuild/pex)

[pipx · PyPI](https://pypi.org/project/pipx/)

### PyInstaller

[Welcome to PyInstaller official website](http://www.pyinstaller.org/)
[PyInstaller Manual — PyInstaller documentation](https://pyinstaller.readthedocs.io/en/latest/)
[pyinstaller/pyinstaller: Freeze (package) Python programs into stand-alone executables](https://github.com/pyinstaller/pyinstaller)

[How to deploy PyQt, Keras, Tensorflow apps with PyInstaller - YouTube](https://www.youtube.com/watch?v=fLQg8dgB7cA)
PyInstaller did what cx_Freeze failed, with 300MB less size.
This is done possibly with tree shaking.

[Introducing PyInstaller | Linux Journal](https://www.linuxjournal.com/content/introducing-pyinstaller)
[Using PyInstaller to Easily Distribute Python Applications – Real Python](https://realpython.com/pyinstaller-python/)

[FAQ · pyinstaller/pyinstaller Wiki](https://github.com/pyinstaller/pyinstaller/wiki/FAQ)
[Recipes · pyinstaller/pyinstaller Wiki](https://github.com/pyinstaller/pyinstaller/wiki/Recipes)

[When Things Go Wrong — PyInstaller documentation](https://pyinstaller.readthedocs.io/en/stable/when-things-go-wrong.html)

When debugging:

- check `build\{NAME}\` for logs
- check debug messages:

  ```sh
  pyinstaller --clean -y --log-level=DEBUG specfile 2> build.log
  ```

- run bundled app at console to see error log
- use onedir to view bundle structure easily, also `pyi-archive_viewer`

setuptools 45 breaks PyInstaller ("Failed to execute script pyi_rth_pkgres"), downgrade to 44 until this is fixed
[setuptools 45.0.0 may cause PyInstaller 3.3 packaged executable fail to launch · Issue #1963 · pypa/setuptools](https://github.com/pypa/setuptools/issues/1963)

- use latest version
  pip install https://github.com/pyinstaller/pyinstaller/archive/master.zip

```sh
pip install --upgrade 'setuptools<45.0.0'
```

#### Hooks

[Understanding PyInstaller Hooks — PyInstaller documentation](https://pythonhosted.org/PyInstaller/hooks.html)
[pyinstaller/PyInstaller/hooks at master · pyinstaller/pyinstaller](https://github.com/pyinstaller/pyinstaller/tree/master/PyInstaller/hooks)

[Trouble with Tensorflow 2.0 · Issue #4400 · pyinstaller/pyinstaller](https://github.com/pyinstaller/pyinstaller/issues/4400) `hook-tensorflow_core.py`
[Python, Pandas, & PyInstaller — Watch Out! - Nathan Benton - Medium](https://medium.com/@nbenton90/python-pandas-pyinstaller-watch-out-5d9af2cea867)
[Pyinstaller hooks — Kivy 1.11.1 documentation](https://kivy.org/doc/stable/api-kivy.tools.packaging.pyinstaller_hooks.html)

### cx_Freeze

[cx_Freeze](https://anthony-tuininga.github.io/cx_Freeze/)
[Welcome to cx_Freeze’s documentation!](http://cx-freeze.readthedocs.io/en/latest/)
[cx_Freeze](http://web.archive.org/web/20120622213400/http://cx-freeze.sourceforge.net/cx_Freeze.html)

Your source code is put in `lib/library.zip`, some tricks is needed to add data to the bundle.
This is the bundled folder structure:

```
build/exe.linux-x86_64-3.7/
- lib/library.zip
- ui/
- main
```

The aim is to load asset from `ui/` from scripts packaged in `lib/library.zip`.

```python
# freeze helper
from os import path
import sys

if getattr(sys, "frozen", False):
    # The application is frozen
    print(f"frozen app, exec='{sys.executable}'")
    ASSET_DIR = path.dirname(sys.executable)
else:
    # The application is not frozen
    # Change this bit to match where you store your data files:
    ASSET_DIR = path.dirname(__file__)
```

```python
# setup.py
import sys
from cx_Freeze import setup, Executable

# Dependencies are automatically detected, but it might need
# fine tuning.
includeFiles = ["ui"]
buildOptions = dict(packages=[], excludes=[], include_files=includeFiles)

base = "Win32GUI" if sys.platform == "win32" else None

executables = [Executable("main.py", base=base)]
setup(
    name="demo",
    version="1.0",
    description="",
    options=dict(build_exe=buildOptions),
    executables=executables,
)
```

```sh
python setup.py build
```

## Linters

[Python Code Quality Authority](https://github.com/PyCQA)
[An Introduction to the PyCQA](http://meta.pycqa.org/en/latest/introduction.html)
[Python Code Quality: Tools & Best Practices – Real Python](https://realpython.com/python-code-quality/) !important
[7 Python libraries for more maintainable code | Opensource.com](https://opensource.com/article/18/7/7-python-libraries-more-maintainable-code)

[Auto formatters for Python 👨‍💻🤖 - 3YOURMIND-Tech - Medium](https://medium.com/3yourmind/auto-formatters-for-python-8925065f9505)

[ambv/black: The uncompromising Python code formatter](https://github.com/ambv/black)
[The uncompromising code formatter — Black documentation](https://black.readthedocs.io/en/stable/)

[google/yapf: A formatter for Python files](https://github.com/google/yapf)

[Flake8: Your Tool For Style Guide Enforcement](http://flake8.pycqa.org/en/latest/index.html)
[Pylint User Manual](https://pylint.readthedocs.io/en/latest/) generates too much warning
[pycodestyle’s documentation](https://pycodestyle.readthedocs.io/en/latest/) pycodestyle is the new pep8

[Pylint vs flake8 detailed comparison as of 2017 - Slant](https://www.slant.co/versus/12630/12632/~pylint_vs_flake8)
[python - PyLint, PyChecker or PyFlakes? - Stack Overflow](http://stackoverflow.com/questions/1428872/pylint-pychecker-or-pyflakes)

[Refactoring Python Applications for Simplicity – Real Python](https://realpython.com/python-refactoring/)
[Python Code Quality: Tools & Best Practices – Real Python](https://realpython.com/python-code-quality/)

[What is wily? — wily develop documentation](https://wily.readthedocs.io/en/latest/)
[Anthony Shaw - Wily Python: Writing simpler and more maintainable Python - PyCon 2019 - YouTube](https://www.youtube.com/watch?v=dqdsNoApJ80)

[Welcome to Radon’s documentation! — Radon documentation](https://radon.readthedocs.io/en/latest/)
[rubik/radon: Various code metrics for Python code](https://github.com/rubik/radon)

[Pysa: Open Source static analysis for Python code - Facebook Engineering](https://engineering.fb.com/security/pysa/)

## Type hints/Typing

Python 3.5 adds type hints to functions, 3.6 extends that for variable.
3.10 support type guards/type narrowing
Type Guard: boolean value that have implication to type of variables of union type
[PEP 647 -- User-Defined Type Guards | Python.org](https://www.python.org/dev/peps/pep-0647/)

[PEP 484 -- Type Hints | Python.org](https://www.python.org/dev/peps/pep-0484/)
[Our journey to type checking 4 million lines of Python | Dropbox Tech Blog](https://blogs.dropbox.com/tech/2019/09/our-journey-to-type-checking-4-million-lines-of-python/)

[The Ultimate Guide to Python Type Checking – Real Python](https://realpython.com/python-type-checking/) !important
[the state of type hints in Python](https://www.bernat.tech/the-state-of-type-hints-in-python/)
[Stanford Seminar - Optional Static Typing for Python - YouTube](https://www.youtube.com/watch?v=GiZKuyLKvAA)
[Types at the edges in Python – MeadSteve's Dev Blog](https://blog.meadsteve.dev/programming/2020/02/10/types-at-the-edges-in-python/)
[Modernize Your Sinful Python Code with Beautiful Type Hints | by Eirik Berge | Jul, 2021 | Towards Data Science](https://towardsdatascience.com/modernize-your-sinful-python-code-with-beautiful-type-hints-4e72e98f6bf1?gi=85e63db703d4)

[typing — Support for type hints — Python documentation](https://docs.python.org/3/library/typing.html)
[Type hints cheat sheet (Python 3) — Mypy documentation](https://mypy.readthedocs.io/en/latest/cheat_sheet_py3.html)
[How to Use Static Type Checking in Python 3.6 – Adam Geitgey – Medium](https://medium.com/@ageitgey/learn-how-to-use-static-type-checking-in-python-3-6-in-10-minutes-12c86d72677b)
[Python Type Checking (Guide) – Real Python](https://realpython.com/python-type-checking/)
[Using Python's Type Annotations - DEV Community 👩‍💻👨‍💻](https://dev.to/dstarner/using-pythons-type-annotations-4cfe)
[Python type annotations | Caktus Group](https://www.caktusgroup.com/blog/2017/02/22/python-type-annotations/)
[python/typeshed: Collection of library stubs for Python, with static types](https://github.com/python/typeshed)

"advanced-python-typing" series
[1-minute guide to real constants in Python - DEV Community 👩‍💻👨‍💻](https://dev.to/wemake-services/1-minute-guide-to-real-constants-in-python-2bpk)

[Type-Checking Python Programs With Type Hints and mypy - YouTube](https://www.youtube.com/watch?v=2xWhaALHTvU)
[Carl Meyer - Type-checked Python in the real world - PyCon 2018 - YouTube](https://www.youtube.com/watch?v=pMgmKJyWKn8)

Mypy can be used to do static type checking on type hints.  
[mypy - Optional Static Typing for Python](http://mypy-lang.org/)
[Welcome to Mypy documentation! — Mypy documentation](https://mypy.readthedocs.io/en/latest/)
[Introducing Mypy, an Experimental Optional Static Type Checker for Python | Linux Journal](https://www.linuxjournal.com/content/introducing-mypy-experimental-optional-static-type-checker-python)
[Python's Mypy--Advanced Usage | Linux Journal](https://www.linuxjournal.com/content/pythons-mypy-advanced-usage)
[Mypy improves static type-checking for big Python apps | InfoWorld](https://www.infoworld.com/article/3066749/application-development/mypy-improves-static-type-checking-for-big-python-apps.html)
[How Mypy could simplify compiling Python | InfoWorld](http://www.infoworld.com/article/3148718/open-source-tools/how-mypy-could-simplify-compiling-python.html)

[microsoft/pyright: Static type checker for Python](https://github.com/microsoft/pyright)

[Instagram/MonkeyType: A system for Python that generates static type annotations by collecting runtime types](https://github.com/instagram/MonkeyType)

advanced-python-typing (7 Part Series)
[1-minute guide to real constants in Python - DEV Community 👩‍💻👨‍💻](https://dev.to/wemake-services/1-minute-guide-to-real-constants-in-python-2bpk)
[Simple dependent types in Python - DEV Community 👩‍💻👨‍💻](https://dev.to/wemake-services/simple-dependent-types-in-python-4e14)
[Python exceptions considered an anti-pattern - DEV Community 👩‍💻👨‍💻](https://dev.to/wemake-services/python-exceptions-considered-an-anti-pattern-17o9)

[Pyre · A performant type-checker for Python 3](https://pyre-check.org/) Facebook
[Overview · Pyre](https://pyre-check.org/docs/overview.html)
[Pieter Hooimeijer - Types, Deeper Static Analysis, and you - PyCon 2018 - YouTube](https://www.youtube.com/watch?v=hWV8t494N88)

[google/pytype: A static type analyzer for Python code](https://github.com/google/pytype) Google

[prechelt/typecheck-decorator: For Python3, e.g. @typecheck add_count(count: int, when: any(datetime, timedelta) = datetime.now)](https://github.com/prechelt/typecheck-decorator)

[Instagram/MonkeyType: A system for Python that generates static type annotations by collecting runtime types](https://github.com/Instagram/MonkeyType)

[pydantic](https://pydantic-docs.helpmanual.io/) Data validation and settings management using python type annotations
[samuelcolvin/pydantic: Data validation using Python type hinting](https://github.com/samuelcolvin/pydantic)

## WinPython

[WinPython](http://winpython.github.io/)

## List installed packages

```sh
pip list
pip freeze
```
