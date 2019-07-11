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

[Presentations & Blog Posts — Conda documentation](http://conda.pydata.org/docs/)
[Anaconda Distribution | Continuum Analytics: Documentation](https://docs.continuum.io/anaconda/)

[Python Module of the Week - Python Module of the Week](https://pymotw.com/2/index.html)
[Python 3 Module of the Week — PyMOTW 3](https://pymotw.com/3/)
[dhellmann / PyMOTW-3 — Bitbucket](https://bitbucket.org/dhellmann/pymotw-3/)

[mitsuhiko/pipsi: pip script installer](https://github.com/mitsuhiko/pipsi) installs to virtualenv

[Welcome to the tox automation project — tox documentation](https://tox.readthedocs.io/en/latest/)

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

### `pip-tools`

> principals adopted by `pipenv`

[jazzband/pip-tools: A set of tools to keep your pinned Python dependencies fresh.](https://github.com/jazzband/pip-tools)

[Better Package Management » nvie.com](https://nvie.com/posts/better-package-management/)

### `poetry`

[sdispater/poetry: Python dependency management and packaging made easy.](https://github.com/sdispater/poetry) also build and publish packages

[Poetry - Python dependency management and packaging made easy.](https://poetry.eustace.io/)

## Virtual Environments

> use `pipenv`

[28.3. venv — Creation of virtual environments — Python 3 documentation](https://docs.python.org/3/library/venv.html)
[Virtualenv — virtualenv documentation](https://virtualenv.pypa.io/en/latest/)
[Deepwalker/pundler: Python bundler-alike alternative to virtualenv](https://github.com/Deepwalker/pundler)

[Virtualenv and venv: Python virtual environments explained | InfoWorld](https://www.infoworld.com/article/3239675/python/virtualenv-and-venv-python-virtual-environments-explained.html)
[pyvenv vs virtualenv : learnpython](https://www.reddit.com/r/learnpython/comments/4hsudz/pyvenv_vs_virtualenv/)

[Python Virtual Environments – A Primer – Real Python](https://realpython.com/python-virtual-environments-a-primer/)
[Using virtual environments with Python ~ The Python Corner](https://www.thepythoncorner.com/2018/05/using-virtual-environments-withpython.html)

### pipenv

`pipenv` is the recommend package management tool by PyPA and the reference implementation for [Pipfile](https://github.com/pypa/pipfile) (`requirements.txt` replacement). It creates virtualenv in `~/.local/share/virtualenvs` instead of project folder.

[Pipenv: Python Dev Workflow for Humans — pipenv documentation](https://docs.pipenv.org/)
[pypa/pipenv: Python Development Workflow for Humans.](https://github.com/pypa/pipenv)
[Kenneth Reitz - Pipenv: The Future of Python Dependency Management - PyCon 2018 - YouTube](https://www.youtube.com/watch?v=GBQAKldqgZs&index=138)

[Pipenv: A Guide to the New Python Packaging Tool – Real Python](https://realpython.com/pipenv-guide/)

Issues:

- for application only, not for libraries
- py2 and py3 cannot co-exist
- locked to a single minor version of Python  
  often reporting version mismatch when running script in other environment
- no QA before release
- [Why is pipenv the recommended packaging tool by the community and PyPA? : Python](https://www.reddit.com/r/Python/comments/8jd6aq/why_is_pipenv_the_recommended_packaging_tool_by/)

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

[Better Python version and environment management with pyenv](http://fgimian.github.io/blog/2014/04/20/better-python-version-and-environment-management-with-pyenv/)
[Python, Developersetup, Howto by Fröhlich ∧ Frei](https://www.froehlichundfrei.de/blog/2014-11-30-my-transition-to-python3-and-pyenv-goodby-virtualenvwrapper/)
[pyenv/pyenv-installer: This tool is used to install `pyenv` and friends.](https://github.com/pyenv/pyenv-installer)

### virtualenv

> it is a little troublesome to setup

[Virtualenv](https://virtualenv.pypa.io/en/stable/) create python environment in local folder
[virtualenvwrapper documentation](https://virtualenvwrapper.readthedocs.io/en/latest/) create python environment in a centralized folder
[Virtualenv vs Virtualenvwrapper · Saurabh Kumar](https://saurabh-kumar.com/blog/virtualenv-vs-virtualenvwrapper.html) !important

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

## Packages

```sh
sudo pip install TermRecord
sudo pip install git-up
sudo pip install ngxtop
sudo pip install python-pygame

pip install --user ipython black pyls-black
```

[Hidden gems: 14 Python libraries too good to overlook | InfoWorld](http://www.infoworld.com/article/3164409/application-development/hidden-gems-14-python-libraries-too-good-to-overlook.html)
[6 Python libraries every programmer will love | InfoWorld](http://www.infoworld.com/article/3008915/application-development/6-python-libraries-every-programmer-will-love.html)
[4 can't-miss Python goodies from Microsoft, Google, Facebook, and Uber | InfoWorld](http://www.infoworld.com/article/3126468/application-development/4-cant-miss-python-goodies-from-microsoft-google-facebook-and-uber.html)

[Trey Hunner](http://treyhunner.com/)
[Splinter documentation](https://splinter.readthedocs.io/en/latest/)
[Python 3 Module of the Week — PyMOTW 3](https://pymotw.com/3/)

[5 wicked-fast Python frameworks you have to try | InfoWorld](http://www.infoworld.com/article/3133854/application-development/5-wicked-fast-python-frameworks-you-have-to-try.html)

[Sending Emails With Python – Real Python](https://realpython.com/python-send-email/)

[mahmoud/boltons: 🔩 Like builtins, but boltons. Constructs/recipes/snippets that would be handy in the standard library. Nothing like Michael Bolton.](https://github.com/mahmoud/boltons)

[bwasti/cache.py: Python memoization across program runs.](https://github.com/bwasti/cache.py)

[keleshev/schema: Schema validation just got Pythonic](https://github.com/keleshev/schema)

[santinic/pampy: Pampy: The Pattern Matching for Python you always dreamed of.](https://github.com/santinic/pampy)

[Requests: HTTP for Humans™ — Requests documentation](http://docs.python-requests.org/en/master/)
[kennethreitz/requests: Python HTTP Requests for Humans™](https://github.com/kennethreitz/requests)
[Requests-HTML: HTML Parsing for Humans (writing Python 3)! — requests-HTML documentation](https://html.python-requests.org/)

[kennethreitz/maya: Datetimes for Humans™](https://github.com/kennethreitz/maya)
[kennethreitz/delegator.py: Subprocesses for Humans 2.0.](https://github.com/kennethreitz/delegator.py)
[Arrow: better dates and times for Python](http://arrow.readthedocs.io/en/latest/)

### Web Frameworks

[Python Web Frameworks To Learn In 2018 | Python Frameworks | Mindfire](http://www.mindfiresolutions.com/blog/2018/03/python-web-frameworks-2018/)
[Review: 13 Python web frameworks compared | InfoWorld](https://www.infoworld.com/article/3105502/python/review-13-python-web-frameworks-compared.html)

[A familiar HTTP Service Framework — responder 1.1.3 documentation](https://python-responder.org/en/latest/)

#### Flask

[Welcome | Flask (A Python Microframework)](http://flask.pocoo.org/)
[humiaozuzu/awesome-flask: A curated list of awesome Flask resources and plugins](https://github.com/humiaozuzu/awesome-flask)

[Extensions Registry | Flask (A Python Microframework)](http://flask.pocoo.org/extensions/)
[Flask-RESTPlus documentation](https://flask-restplus.readthedocs.io/en/stable/)

[Miguel Grinberg - Flask Workshop - PyCon 2015 - YouTube](https://www.youtube.com/watch?v=DIcpEg77gdE)
[Miguel Grinberg - Flask at Scale - PyCon 2016 - YouTube](https://www.youtube.com/watch?v=tdIIJuPh3SI)
[miguelgrinberg/flack: Companion code to my PyCon 2016 "Flask at Scale" tutorial session.](https://github.com/miguelgrinberg/flack)
[Miguel Grinberg - Microservices with Python and Flask - PyCon 2017 - YouTube](https://www.youtube.com/watch?v=nrzLdMWTRMM)
[BUILDING MICROSERVICES WITH PYTHON AND FLASK - YouTube](https://www.youtube.com/watch?v=1X3_gQwfabI)
[Flask web development with Python - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDcOS4l8RCWh0olq_je0OKaP)
[Practical Flask Web Development Tutorials - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDc_owjTbIY4rbgXOFkUYOUB)

[Python REST APIs With Flask, Connexion, and SQLAlchemy – Real Python](https://realpython.com/flask-connexion-rest-api/)
[Python REST APIs With Flask, Connexion, and SQLAlchemy – Part 2 – Real Python](https://realpython.com/flask-connexion-rest-api-part-2/)
[Python REST APIs With Flask, Connexion, and SQLAlchemy – Part 3 – Real Python](https://realpython.com/flask-connexion-rest-api-part-3/)

[Creating REST Services With Flask - DZone Integration](https://dzone.com/articles/creating-rest-services-with-flask)
[Get started writing your own web services using Python Flask | Opensource.com](https://opensource.com/article/17/3/writing-web-service-using-python-flask)

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

#### Django

> see `django.md`

#### Honerable Mentions

[Bottle: Python Web Framework — Bottle 0.13-dev documentation](http://bottlepy.org/docs/dev/)
[bottlepy/bottle: bottle.py is a fast and simple micro-framework for python web-applications.](https://github.com/bottlepy/bottle)

[CherryPy — A Minimalist Python Web Framework](https://cherrypy.org/)
[cherrypy/cherrypy: CherryPy is a pythonic, object-oriented HTTP framework. https://docs.cherrypy.org/](https://github.com/cherrypy/cherrypy)

[www.web2py.com](http://www.web2py.com/)
[web2py - Preface](http://web2py.com/book) the manual
[Welcome to web2py’s API documentation!](http://web2py.readthedocs.io/en/latest/)
[web2py video course 2013 on Vimeo](https://vimeo.com/album/3016728)

[jczic/MicroWebSrv: A micro HTTP Web server that supports WebSockets, html/python language templating and routing handlers, for MicroPython (used on Pycom modules & ESP32)](https://github.com/jczic/MicroWebSrv)
[channelcat/sanic: Async Python 3.5+ web server that's written to go fast](https://github.com/channelcat/sanic)
[encode/apistar: A smart Web API framework, designed for Python 3. 🌟](https://github.com/encode/apistar)
[molten: modern API framework — molten 0.1.0 documentation](https://moltenframework.com/)

### Logging

[16.6. logging — Logging facility for Python — Python 3 documentation](https://docs.python.org/3/library/logging.html)
[Logging HOWTO — Python 3.7.3 documentation](https://docs.python.org/3/howto/logging.html)
[Logging Cookbook — Python 3 documentation](https://docs.python.org/3/howto/logging-cookbook.html)
[A guide to logging in Python | Opensource.com](https://opensource.com/article/17/9/python-logging)
[Python Logging: In-Depth Tutorial | Toptal](https://www.toptal.com/python/in-depth-python-logging)
[Logging in Python ~ The Python Corner](https://www.thepythoncorner.com/2018/05/logging-in-python.html)

[Logging in Python – Real Python](https://realpython.com/python-logging/)
[Python Logging: A Stroll Through the Source Code – Real Python](https://realpython.com/python-logging-source-code/)

[Python's Built-In 'logging' Module - YouTube](https://www.youtube.com/watch?v=4t67SNWoPxk)

### FUSE

[fusepy/fusepy: Simple ctypes bindings for FUSE](https://github.com/fusepy/fusepy)

[Writing a FUSE filesystem in Python – The Python corner – Medium](https://medium.com/the-python-corner/writing-a-fuse-filesystem-in-python-5e0f2de3a813)
[Writing a FUSE filesystem in Python - Stavros' Stuff](https://www.stavros.io/posts/python-fuse-filesystem/)
[skorokithakis/python-fuse-sample: A sample FUSE filesystem in Python.](https://github.com/skorokithakis/python-fuse-sample)

### PDF

[PyPDF2 Documentation](https://pythonhosted.org/PyPDF2/)
[How to Work With a PDF in Python – Real Python](https://realpython.com/pdf-python/)
[An Intro to PyPDF2 | The Mouse Vs. The Python](https://www.blog.pythonlibrary.org/2018/06/07/an-intro-to-pypdf2/)

[ReportLab open-source PDF Toolkit - ReportLab.com](https://www.reportlab.com/opensource/)
[Reportlab | The Mouse Vs. The Python](http://www.blog.pythonlibrary.org/tag/reportlab/)
[A Simple Step-by-Step Reportlab Tutorial | The Mouse Vs. The Python](https://www.blog.pythonlibrary.org/2010/03/08/a-simple-step-by-step-reportlab-tutorial/)
[ReportLab 101: The textobject | The Mouse Vs. The Python](http://www.blog.pythonlibrary.org/2018/02/06/reportlab-101-the-textobject/)

[PDFMiner](https://euske.github.io/pdfminer/)

### Async I/O

[Comparing gevent to eventlet | Concurrency in Python](https://blog.gevent.org/2010/02/27/why-gevent/)
[What is gevent? — gevent documentation](http://www.gevent.org/) uses libev

[Eventlet Networking Library](http://eventlet.net/)

[MagicStack/uvloop: Ultra fast asyncio event loop.](https://github.com/MagicStack/uvloop)

[18.5. asyncio — Asynchronous I/O, event loop, coroutines and tasks — Python 3 documentation](https://docs.python.org/3/library/asyncio.html)
[asyncio — Asynchronous I/O, event loop, and concurrency tools — PyMOTW 3](https://pymotw.com/3/asyncio/)
[pymotw3/source/asyncio at master · reingart/pymotw3](https://github.com/reingart/pymotw3/tree/master/source/asyncio)
[Asyncio Documentation — Asyncio Documentation documentation](http://asyncio.readthedocs.io/en/latest/index.html)

[Welcome to AIOHTTP — aiohttp documentation](https://aiohttp.readthedocs.io/en/stable/)

[Trio: async programming for humans and snake people](https://trio.readthedocs.io/en/latest/)

[Unsync](http://asherman.io/projects/unsync.html)
[alex-sherman/unsync: Unsynchronize asyncio](https://github.com/alex-sherman/unsync)

### Socket programming

[19.1. socket — Low-level networking interface — Python 3 documentation](https://docs.python.org/3/library/socket.html)
[22.21. socketserver — A framework for network servers — Python 3 documentation](https://docs.python.org/3/library/socketserver.html)

[Socket Programming in Python (Guide) – Real Python](https://realpython.com/python-sockets/)

### Distributed Computing

[execnet: Distributed Python deployment and communication](http://codespeak.net/execnet/)

[Homepage | Celery: Distributed Task Queue](http://www.celeryproject.org/)

[rq/rq: Simple job queues for Python](https://github.com/rq/rq)
[RQ: Simple job queues for Python](https://python-rq.org/)
[Introducing RQ » nvie.com](https://nvie.com/posts/introducing-rq/)

[closeio/tasktiger: Python task queue. Because celery is gross.](https://github.com/closeio/tasktiger)

### Image manipulation

[Wand documentation](http://docs.wand-py.org/en/latest/index.html#)
[ImageMagick/PythonMagick: PythonMagick](https://github.com/ImageMagick/PythonMagick)
[python - Documents and examples of PythonMagick - Stack Overflow](http://stackoverflow.com/questions/1740158/documents-and-examples-of-pythonmagick/5188661#5188661)

[Python Imaging Library (PIL)](http://www.pythonware.com/products/pil/)
[Pillow — Pillow (PIL Fork) documentation](http://pillow.readthedocs.io/en/latest/)
`python-image` of most distro points to `pillow`

### Database/ORM

[Object-relational Mappers (ORMs) - Full Stack Python](https://www.fullstackpython.com/object-relational-mappers-orms.html)

[SQLAlchemy - The Database Toolkit for Python](http://www.sqlalchemy.org/)
[dahlia/awesome-sqlalchemy: A curated list of awesome tools for SQLAlchemy](https://github.com/dahlia/awesome-sqlalchemy)

[GitHub - coleifer/peewee: a small, expressive orm -- supports postgresql, mysql and sqlite](https://github.com/coleifer/peewee)
[kennethreitz/records: SQL for Humans™](https://github.com/kennethreitz/records)
[MagicStack/asyncpg: A fast PostgreSQL Database Client Library for Python/asyncio.](https://github.com/MagicStack/asyncpg)

### Serialization

[12.1. pickle — Python object serialization — Python 3 documentation](https://docs.python.org/3/library/pickle.html)

[Serialization and Deserialization of Python Objects: Part 1](https://code.tutsplus.com/tutorials/serialization-and-deserialization-of-python-objects-part-1--cms-26183)
[Serialization and Deserialization of Python Objects: Part 2](https://code.tutsplus.com/tutorials/serialization-and-deserialization-of-python-objects-part-2--cms-26184)
[Object serialization in Python ~ The Python Corner](https://www.thepythoncorner.com/2018/05/object-serialization-inpython.html)

[construct/construct: Construct: Declarative data structures for python that allow symmetric parsing and building](https://github.com/construct/construct)

[Serialize · PyPI](https://pypi.org/project/Serialize/)

[serpent · PyPI](https://pypi.org/project/serpent/)

[marshmallow · PyPI](https://pypi.org/project/marshmallow/)

[serpy: ridiculously fast object serialization — serpy documentation](https://serpy.readthedocs.io/en/latest/)
[JSON Serialization in Python using serpy – Twilio Cloud Communications Blog](https://www.twilio.com/blog/2017/08/json-serialization-in-python-using-serpy.html)

[Better Python Object Serialization · Homepage of Hynek Schlawack](https://hynek.me/articles/serialization/)

### CLI

[Comparing Python Command-Line Parsing Libraries - Argparse, Docopt, and Click - Real Python](https://realpython.com/blog/python/comparing-python-command-line-parsing-libraries-argparse-docopt-click/)

[16.4. argparse — Parser for command-line options, arguments and sub-commands — Python 3.6.0 documentation](https://docs.python.org/3/library/argparse.html)
[Python Argparse Cookbook - mkaz.tech](https://mkaz.tech/code/python-argparse-cookbook.html)
[PEP 389 -- argparse - New Command Line Parsing Module | Python.org](https://www.python.org/dev/peps/pep-0389/)
[Python Argparse Cookbook – mkaz.blog](https://mkaz.blog/code/python-argparse-cookbook/)
[Learn Enough Python to be Useful: argparse – Towards Data Science](https://towardsdatascience.com/learn-enough-python-to-be-useful-argparse-e482e1764e05)

[Welcome to the Click Documentation](http://click.pocoo.org/)
[Writing Python Command-Line Tools With Click – dbader.org](https://dbader.org/blog/python-commandline-tools-with-click)
[Mastering Click: Writing Advanced Python Command-Line Apps – dbader.org](https://dbader.org/blog/mastering-click-advanced-python-command-line-apps)

[OpenStack Docs: cliff – Command Line Interface Formulation Framework](https://docs.openstack.org/cliff/latest/)

[docopt—language for description of command-line interfaces](http://docopt.org/)
[Python argparse: Make at least one argument required - Stack Overflow](https://stackoverflow.com/questions/6722936/python-argparse-make-at-least-one-argument-required) docopt example

[Cement Framework](https://builtoncement.com/)

[google/python-fire: Python Fire is a library for automatically generating command line interfaces (CLIs) from absolutely any Python object.](https://github.com/google/python-fire)

[kennethreitz/clint: Python Command-line Application Tools](https://github.com/kennethreitz/clint)
[kennethreitz/crayons: Text UI colors for Python.](https://github.com/kennethreitz/crayons)

[jonathanslenders/python-prompt-toolkit: Library for building powerful interactive command lines in Python](https://github.com/jonathanslenders/python-prompt-toolkit)

[Pytabby: a tabbed menu system for console-based Python programs - DEV Community 👩‍💻👨‍💻](https://dev.to/prooffreader/pytabby-a-tabbed-menu-system-for-console-based-python-programs-301n)
[tqdm/tqdm: A fast, extensible progress bar for Python and CLI](https://github.com/tqdm/tqdm)
[tqdm documentation](https://tqdm.github.io/)

[GitHub - amoffat/sh: Python process launching](https://github.com/amoffat/sh)

[GitHub - chriskiehl/Gooey: Turn (almost) any Python command line program into a full GUI application with one line](https://github.com/chriskiehl/Gooey)

### Project Generator

[Cookiecutter: Better Project Templates — cookiecutter documentation](http://cookiecutter.readthedocs.io/en/latest/)

[Raphael Pierzina - Kickstarting projects with Cookiecutter - YouTube](https://www.youtube.com/watch?v=nExL0SgKsDY)

[Cookiecutter Templates](http://cookiecutter-templates.sebastianruml.name/)
[nvie/cookiecutter-python-cli](https://github.com/nvie/cookiecutter-python-cli)

### GUI

[PyQt](https://github.com/pyqt)
[PyQt Tutorial](https://www.tutorialspoint.com/pyqt/index.htm)
[Python Programming Tutorials](https://pythonprogramming.net/basic-gui-pyqt-tutorial/)
[Riverbank | Software | PyQt | What is PyQt?](https://riverbankcomputing.com/software/pyqt/intro)
[PyQt5 Reference Guide](http://pyqt.sourceforge.net/Docs/PyQt5/)
[User Guide — dip documentation](http://pyqt.sourceforge.net/Docs/dip/) for writing resuable UI component
[pyqtdeploy User Guide](http://pyqt.sourceforge.net/Docs/pyqtdeploy/)

[Graphical User Interfaces with Tk — Python 3 documentation](https://docs.python.org/3/library/tk.html)
[TkDocs Home](https://tkdocs.com/)
[Tkinter 8.5 reference: a GUI for Python](http://infohost.nmt.edu/tcc/help/pubs/tkinter/web/index.html)
[Python GUI Guide: Introduction to Tkinter - learn.sparkfun.com](https://learn.sparkfun.com/tutorials/python-gui-guide-introduction-to-tkinter/all)
[guizero documentation](https://lawsie.github.io/guizero/about/) modern API on Tkinter
install `tcl` and `tk` on host first
Forget Tkinter, which is designed 20 years ago.

[VPython](https://vpython.org/)

[PyGTK](http://www.pygtk.org/)
[The Python GTK+ 3 Tutorial — Python GTK+ 3 Tutorial 3.4 documentation](https://python-gtk-3-tutorial.readthedocs.io/en/latest/index.html)

[PyForms](https://pyforms.readthedocs.io/en/latest/) consistent UI on desktop, web and terminal

[Add GUIs to your programs and scripts easily with PySimpleGUI | Opensource.com](https://opensource.com/article/18/8/pysimplegui)
[MikeTheWatchGuy/PySimpleGUI: Launched in 2018 Actively developed and supported](https://github.com/MikeTheWatchGuy/PySimpleGUI)
[PySimpleGUI](https://pysimplegui.readthedocs.io/)

[Welcome to wxPython! | wxPython](https://www.wxpython.org/)
[wxForty-Two Blog | wxPython](https://www.wxpython.org/blog/)

[Toga— BeeWare](https://pybee.org/project/projects/libraries/toga/)

[pyglet / pyglet / wiki / Home — Bitbucket](https://bitbucket.org/pyglet/pyglet/wiki/Home)
[pyglet documentation](https://pyglet.readthedocs.io/en/pyglet-1.3-maintenance/)

[EasyGUI — easygui documentation](http://easygui.sourceforge.net/index.html)

[PySide - Qt Wiki](https://wiki.qt.io/PySide) old Qt binding

### eBook

[Overview — Sphinx documentation](http://www.sphinx-doc.org/en/stable/)
[GitHub - aerkalov/ebooklib: Python E-book library for handling books in EPUB2/EPUB3 and Kindle format -](https://github.com/aerkalov/ebooklib/)
[GitHub - anqxyr/mkepub: Simple minimalistic library for creating EPUB3 files](https://github.com/anqxyr/mkepub)

## Distribution

[A tutorial on packaging up your Python code for PyPI](https://snarky.ca/a-tutorial-on-python-package-building/)
[Building a Python API for Raspberry Pi hardware - Speaker Deck](https://speakerdeck.com/bennuttall/building-a-python-api-for-raspberry-pi-hardware)

[Packaging Python Projects — Python Packaging User Guide](https://packaging.python.org/tutorials/packaging-projects/)
[Packaging and Distributing Projects — Python Packaging User Guide](https://packaging.python.org/tutorials/distributing-packages/)
[Packaging and distributing projects — Python Packaging User Guide](https://packaging.python.org/guides/distributing-packages-using-setuptools/)
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

[Pipenv: A Guide to the New Python Packaging Tool – Real Python](https://realpython.com/pipenv-guide/#package-distribution) Using `setuptools` with `pipenv`
Put dependencies in `setup.py` instead of `Pipfile`, use `pipenv install -e` to install package locally.

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

[takluyver/flit: Simplified packaging of Python modules](https://github.com/takluyver/flit)
[Flit 1.0 — Flit documentation](https://flit.readthedocs.io/en/latest/) build with `pyproject.toml`

[sdispater/poetry: Python dependency management and packaging made easy.](https://github.com/sdispater/poetry)
[Poetry - Python dependency management and packaging made easy.](https://poetry.eustace.io/) build with `pyproject.toml`

### Standalone Binary

> note: most of these tools do not support Python 3

[cx_Freeze](https://anthony-tuininga.github.io/cx_Freeze/)
[Welcome to cx_Freeze’s documentation!](http://cx-freeze.readthedocs.io/en/latest/)

[Welcome to PyInstaller official website](http://www.pyinstaller.org/)
[PyInstaller Manual — PyInstaller documentation](https://pyinstaller.readthedocs.io/en/latest/)
[Introducing PyInstaller | Linux Journal](https://www.linuxjournal.com/content/introducing-pyinstaller)
[pyinstaller/pyinstaller: Freeze (package) Python programs into stand-alone executables](https://github.com/pyinstaller/pyinstaller)

[schmir/bbfreeze: UNMAINTAINED](https://github.com/schmir/bbfreeze)
[A bbfreeze Tutorial – Build a Binary Series! | The Mouse Vs. The Python](https://www.blog.pythonlibrary.org/2010/08/19/a-bbfreeze-tutorial-build-a-binary-series/)

[`py2exe`](http://www.py2exe.org/) and [`py2app`](https://wiki.python.org/moin/MacPython/py2app) are Windows and OSX specific solution

[Nuitka Home | Nuitka Home](http://nuitka.net/)

[Briefcase](https://briefcase.readthedocs.io/en/latest/)

## Linters

[Python Code Quality Authority](https://github.com/PyCQA)
[An Introduction to the PyCQA](http://meta.pycqa.org/en/latest/introduction.html)
[Python Code Quality: Tools & Best Practices – Real Python](https://realpython.com/python-code-quality/?__s=ynts1awwtp6jpubzzq5f) !important
[7 Python libraries for more maintainable code | Opensource.com](https://opensource.com/article/18/7/7-python-libraries-more-maintainable-code)

[ambv/black: The uncompromising Python code formatter](https://github.com/ambv/black)
[The uncompromising code formatter — Black documentation](https://black.readthedocs.io/en/stable/)

[Flake8: Your Tool For Style Guide Enforcement](http://flake8.pycqa.org/en/latest/index.html)
[Pylint User Manual](https://pylint.readthedocs.io/en/latest/) generates too much warning
[pycodestyle’s documentation](https://pycodestyle.readthedocs.io/en/latest/) pycodestyle is the new pep8

[Pylint vs flake8 detailed comparison as of 2017 - Slant](https://www.slant.co/versus/12630/12632/~pylint_vs_flake8)
[python - PyLint, PyChecker or PyFlakes? - Stack Overflow](http://stackoverflow.com/questions/1428872/pylint-pychecker-or-pyflakes)

## Type Checking

[The Ultimate Guide to Python Type Checking – Real Python](https://realpython.com/python-type-checking/) !important
[26.1. typing — Support for type hints — Python 3.6.5 documentation](https://docs.python.org/3/library/typing.html)
[How to Use Static Type Checking in Python 3.6 – Adam Geitgey – Medium](https://medium.com/@ageitgey/learn-how-to-use-static-type-checking-in-python-3-6-in-10-minutes-12c86d72677b)
[the state of type hints in Python](https://www.bernat.tech/the-state-of-type-hints-in-python/)
[python/typeshed: Collection of library stubs for Python, with static types](https://github.com/python/typeshed)

[mypy - Optional Static Typing for Python](http://mypy-lang.org/)
[Type-Checking Python Programs With Type Hints and mypy - YouTube](https://www.youtube.com/watch?v=2xWhaALHTvU)

[Pyre · A performant type-checker for Python 3](https://pyre-check.org/)
[Overview · Pyre](https://pyre-check.org/docs/overview.html)

"advanced-python-typing" series
[1-minute guide to real constants in Python - DEV Community 👩‍💻👨‍💻](https://dev.to/wemake-services/1-minute-guide-to-real-constants-in-python-2bpk)

[pydantic — pydantic documentation](https://pydantic-docs.helpmanual.io/)
[samuelcolvin/pydantic: Data validation using Python type hinting](https://github.com/samuelcolvin/pydantic)

## WinPython

[WinPython](http://winpython.github.io/)

## List installed packages

```sh
pip list
pip freeze
```
