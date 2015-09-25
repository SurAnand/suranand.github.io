---
layout: post
title: Some things cool about IPython
---

![alt text](http://nbviewer.ipython.org/static/img/example-nb/ipython-thumb.png "IPython")

I am a novice in the land of `Programming`. I am truly enjoying it.

This and the future posts on this kind of subject are only for novices like me. Pros, geeks and wizards, please stay away. You will only end up laughing. ;-)

`IPython` is powerful. Who am I say this, when there giants using it for gigantic projects!

I am learning it and one of the first best learning resources I found really interesting is the 2012 [SciPy Conf](http://conference.scipy.org/scipy2012/tutorials.php#ti-72), **"Intro to NumPy and MatplotLib by Eric Jones"**. Really compelling way of presenting such a technical topic! I made a note of some important usage of IPython beyond the anticipated. I am jotting them down here for my own reference, more than boasting of teaching others.

_**Launch IPython**_

Obviously the beginning is to launch the _environment_ or whatever you call it. I don't even know if I am right calling it an environment, but I thought of the word instantly after watching this lecture for sometime.

Before we launch, let me share a couple more points here. Most generally, programming task expects you to have 3 things ready:

- your favorite text editor (I personally like nano if I am just playing on the shell).
- a terminal sort of shell that enables files/directories navigation.
- and an IDE that interacts with compilers instantly whichever is the language ().

All these along with a vast number of other utilities such as libraries, add-ons etc. are packaged now, especially for python. Two of the most known among those bundles are [Anaconda Python Distribution](https://store.continuum.io/cshop/anaconda/) and [Enthought Canopy](https://www.enthought.com/products/canopy/).

These come as one tarball when you download and with one install command, they create a whole new workspace (or environment) for you to play with almost anything that is possible with python. But it doesn't matter if you don't have them. You can still have the required stuff manually one by one downloaded and installed from your terminal.

Just install ***SciPy*** from their website [here](scipy.org), it comes along with `scipy`, `numpy`, `matplotlib`, the coolest `IPython` and a huge number of other features.

Back to launching ipython for some math, sci-fi stuff like plotting and visualization tasks.

First, if you are on Linux, go to terminal and type `ipython --pylab`.

Or if you are on windows, type `ipython -pylab`.

What this command does is to load your IPython session power-packed. That means it automatically makes ready the essential stuff like, numpy, matplotlib, etc. already loaded. If you just typed ipython and hit enter, you would end up having to type import numpy, import matplotlib, etc. everytime you needed their functionalities in your coding. So the first powerful feature of IPython is the command `ipython --pylab`. So much about launching an app!

***Some Small BIG things you can do with IPython***

_1. WHOS & RESET Commands_

The next cool thing about IPython is the command `whos`.

This gives you the list of variables you created so far in the current session. There already are many other IDEs or shells that may have this sort of feature, but I still like it when IPython does it.

The output of `whos`, it reminds me of how `MySQL` responds in a similar situation. I don't know how `MySQL` understands things, but you ask for its version currently installed on the machine, the current time or date, or anything for that matter (any `Query` technically speaking), it always shows you all of its output in a _data table_ format.

The `whos` command output looks pretty much the same. The opposite of `whos` is `reset` which deletes all the variables created so far. Nice!

***We will continue more on this in another post!***
============================================