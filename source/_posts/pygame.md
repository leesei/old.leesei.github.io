---
title: "Pygame"
date: 2015-01-02 14:10:02
categories:
  - games
tags:
  - game-engine
  - python
  - pygame
  - pygame-zero
toc: true
---

# Pygame

[Pygame](https://www.pygame.org)

- use v2 (with GPU acceleration)
- call `.load()` when loading images

[PyGame on Reddit](https://www.reddit.com/r/pygame/)
[pygame/pygame: pygame (the library) is a Free and Open Source python programming language library for making multimedia applications like games built on top of the excellent SDL library. C, Python, Native, OpenGL.](https://github.com/pygame/pygame)

[Pygame Front Page — pygame v2 documentation](https://www.pygame.org/docs/)
[tutorials - pygame wiki](https://www.pygame.org/wiki/tutorials)
[PyGame: A Primer on Game Programming in Python – Real Python](https://realpython.com/pygame-a-primer/)

[Making Games with Python & Pygame](http://inventwithpython.com/pygame/) book
[Invent Your Own Computer Games with Python](https://inventwithpython.com/chapters/) book
[PyGame with Python 3 Game Development - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDdLkP8MrOXLe_rKuf6r80KO) sentdex
[Python Tutorials - YouTube](https://www.youtube.com/playlist?list=PLWKjhJtqVAbnqBxcdjVGgT3uVR10bzTEB) freeCodeCamp.org
[Pygame Tutorial Series (all) - YouTube](https://www.youtube.com/playlist?list=PLX5fBCkxJmm1fPSqgn9gyR3qih8yYLvMj) DaFluffyPotato

[KidsCanCode.org](http://kidscancode.org/lessons/)
[Game Development with Pygame - YouTube](https://www.youtube.com/playlist?list=PLsk-HSGFjnaH5yghzu7PcOzm9NhsW0Urw)
[Pygame Tutorial #2: Platformer - YouTube](https://www.youtube.com/playlist?list=PLsk-HSGFjnaG-BwZkuAOcVwWldfCLu1pq)
[Pygame Tutorial # 3: Tile-based Game - YouTube](https://www.youtube.com/playlist?list=PLsk-HSGFjnaGQq7ybM8Lgkh5EMxUWPm2i)
[Gamedev: In-depth Topics - YouTube](https://www.youtube.com/playlist?list=PLsk-HSGFjnaHYvbjMbTQG6kLhhZHLzdb3) implements Nature of Code's behavior
[kidscancode/pygame_tutorials: Code to go along with lessons at http://kidscancode.org/lessons](https://github.com/kidscancode/pygame_tutorials)
[kidscancode/gamedev: Example code and docs for "Game Development and Design" class](https://github.com/kidscancode/gamedev)
Basic game loop: float position in state, vector based movements and steering, time based updates
https://github.com/kidscancode/gamedev/blob/master/tutorials/examples/vector_basics.py
https://github.com/kidscancode/gamedev/tree/master/tutorials/examples/steering

[Tech With Tim - YouTube](https://www.youtube.com/channel/UC4JX40jDee_tINbkjycV4Sg/playlists?view=50&sort=dd&shelf_id=6)
[Pygame Programming Tutorials - YouTube](https://www.youtube.com/playlist?list=PLzMcBGfZo4-lp3jAExUCewBfMx3UZFkh5)
[techwithtim/Pygame-Tutorials: This is the code base for the pygame tutorials posted on my YouTube channel.](https://github.com/techwithtim/Pygame-Tutorials)

[Pygame Modules » Raspberry Pi Geek](https://www.raspberry-pi-geek.com/Archive/2014/03/Graphical-displays-with-Python-and-Pygame)

[My First Raspberry Pi Game - YouTube](https://www.youtube.com/playlist?list=PLgyU3jNA6VjS3ij6ZXbb2x4GdEP3bAWzO)
[My First Raspberry Pi Game – Part 01 – Before we start – Andy Balaam's Blog](http://www.artificialworlds.net/blog/2012/10/30/my-first-raspberry-pi-game-part-01-before-we-star/)

## Examples

[Search · pygame](https://github.com/search?l=Python&q=pygame&type=Repositories)
[pygame/examples at master · pygame/pygame](https://github.com/pygame/pygame/tree/master/examples)
[Mekire/pygame-samples: Basic pygame samples illustrating various concepts.](https://github.com/Mekire/pygame-samples)

[serenity-valley/game: A simple game in python with pygame](https://github.com/serenity-valley/game)
[Python Programming Tutorials](https://pythonprogramming.net/pygame-python-3-part-1-intro/)

[Trevor Appleton: Python - Game of Life](http://trevorappleton.blogspot.com/2013/07/python-game-of-life.html)

[Recreate the sprite-following Options from Gradius using Python | Wireframe issue 16 - Raspberry Pi](https://www.raspberrypi.org/blog/recreate-the-sprite-following-options-from-gradius-using-python-wireframe-issue-16/)

[Create a Python game: how to make a puzzle game called Same - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/create-python-game/)
[opethe1st/SameGame: Python implementation of the Same Game using pygame](https://github.com/opethe1st/SameGame)

# Pygame Zero

[Welcome to Pygame Zero — Pygame Zero documentation](https://pygame-zero.readthedocs.io/en/stable/index.html)
[lordmauve/pgzero: A zero-boilerplate games programming framework for Python 3, based on Pygame.](https://github.com/lordmauve/pgzero)

- wrapper for Pygame
- `update()`, `draw()` and input [hooks](https://pygame-zero.readthedocs.io/en/stable/hooks.html)
- automatically load assets from `images/`, `music/`, `sounds/` by file name
- `sounds` only plays `.wav`/`.ogg` and one track at a time
- `music` plays 'mp3'/'ogg'/'oga' in streaming mode and supports multiple track

[Games with PyGame Zero](https://codewith.mu/en/tutorials/1.0/pgzero)
[Code your own 2D shooting gallery in Python | Wireframe issue 20 - Raspberry Pi](https://www.raspberrypi.org/blog/code-your-own-2d-shooting-gallery-in-python-wireframe-issue-20/)
[Teaching a kid to code with Pygame Zero · Matt Layman](https://www.mattlayman.com/blog/2019/teach-kid-code-pygame-zero/)
[Python: let's make a game (Pygame zero) | python programming](https://pythonprogramming.altervista.org/python-making-a-video-game/?doing_wp_cron=1568876414.0923249721527099609375)

## Running game

```sh
pgzrun game.py
```

or

```python
import pgzrun

# your code

pgzrun.go()
```

[runpgzero.py](https://github.com/CoderDojoLu/pgzero-examples/raw/master/runpgzero.py)
[021_gameDevPrimer.py](https://raw.githubusercontent.com/CoderDojoLu/pgzero-examples/master/021_gameDevPrimer.py)

## Pygame Zero’s REPL

```sh
pip3 install pgzero[repl]

pgzrun --repl game.py
```

## Examples

[Search · pygame zero](https://github.com/search?l=Python&q=pygame+zero&type=Repositories)
[pgzero/examples at master · lordmauve/pgzero](https://github.com/lordmauve/pgzero/tree/master/examples)
[CoderDojoLu/pgzero-examples: Some pygame-zero examples](https://github.com/CoderDojoLu/pgzero-examples)
[jzcoder/pgzero-frog-game: Frog & Lilypad game tutorial using Pygame Zero](https://github.com/jzcoder/pgzero-frog-game) game over

### MagPi

[TechnoVisual/Pygame-Zero: Tutorial code for Pygame Zero](https://github.com/TechnoVisual/Pygame-Zero)

[Pygame Zero Invaders - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/pygame-zero-invaders/)
[Pygame Zero: Space Invaders II - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/pygame-zero-space-invaders-ii/) game over and new level

[Code Pac-Man in Python - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/code-pac-man-in-python/) joystick, game over
[Code Pac-Man in Python (part 2) - The MagPi MagazineThe MagPi Magazine](https://www.raspberrypi.org/magpi/code-pac-man-python-part-2/)
