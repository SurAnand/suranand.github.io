---
layout:
title: Floobits & Flootty for Pair Programming
comments: true
---

### On othe offset, I don't really know what *Pair Programming* means!

At least, I am not confident to say I know what it is. But if I just google search with a question like,

> What is pair programming?

It gives me a definition, not so complicated, as shown in the screenshot below.

![alt text](https://github.com/asinode/asinode.github.io/blob/master/public/pairprog.png?raw=true "Pair Programming")

Not so complicated, except for the part where it says "Agile Software Development Technique". I don't want to get into that too. That's an ocean.

## Keep it Simple, Stupid!

Somebody just cried in my ear. So, let me try and say what I understand. Two developers can share their workspace, say a terminal where they run their code, or an editor where they write their code, and work collaboratively. As someone in one of my search results put it, [Floobits](http://floobits.com/) is like Google Docs for developers. While I write the code or run a command in my terminal, you can not only see it in real time, you can actually change my code or command. Does that make enough sense.

I was really excited when I learned about it and quickly made a couple experiments with friends, and they shared my excitement too.

I thought I should keep it here what I have done so far with **Floobits**.

In order to be able to use Floobits, and you are the one who owns the workspace and would like to share it with your partner, you need to do the following things.

- Create a Floobits (obviously, free to begin with ;-) account on their website by signing up.
- Once you login with your new credentials, create a public workspace (5 public workspaces and 1 private workspace come with the free account). Make a note of the URL of your new workspace. Something like `https://floobits.com/username/workspace-name`.
- Go to *Settings* page and get the following.
  - The contents for the `~/.floorc.json` file which you will have to create and save, particularly in your `home` folder.
- Come back to your terminal and ensure you got `python3` with `pip3`.<sup>[1](#myfootnote1)</sup>
- Now you need [Flootty](https://github.com/Floobits/flootty) which is a collaborative terminal, meaning once you have it installed and working, your partner can see and use your terminal.
  - Run `pip install Flootty`
- That's pretty much it. Now, you just need to run,
```sh
flootty --create --url=https://floobits.com/username/workspace-name
```

Let us say, you are the partner and would like to share the workspace with its owner. This is what you need to do.

- Get a Floobits account, similar to the owner step above. But you don't need to create a workspace.
- Get the URL for the owner's workspace.
- Follow the above steps for
  - creating and saving `~/.floorc.json` file in your home folder
  - installing `flootty` with `python3` and `pip3`
- Finally, run this command to join the owner's workspace.
```sh
flootty --url=https://floobits.com/username/workspace-name
```

From this point onward, the owner can go back to the terminal and the partner can see it and also use it.

Now there are two ways you can share the terminal and editor.

1. Use web-based workspace provided by Floobits. This is pretty easy. Just go to the URL of the workspace shared with you and click on the `terminal` on the left menu.
2. Use [Atom IDE](http://atom.io) and install the [Atom Floobits Plugin](https://github.com/Floobits/floobits-atom) from either inside Atom GUI or from terminal using `apm` (Atom Package Manager). All that you can do on the browser-based workspace, you can now do it inside Atom. I am not covering this part for this post. Moreover, in both Atom and the browser-based workspace, you can also do video chat. See the gif below from their [github repo](https://github.com/Floobits/floobits-atom).

<img alt="Editing together in Atom" src="https://camo.githubusercontent.com/41c4615368fc32d0acfb52753631f6e823b46a78/68747470733a2f2f666c6f6f626974732e636f6d2f7374617469632f696d616765732f61746f6d2d656469742e676966" width="640" height="400" data-canonical-src="https://floobits.com/static/images/atom-edit.gif" style="max-width:100%;">

This is very cool and I am sure students should be introduced to tools like this from the very beginning of their learning career.

<a name="myfootnote1">1</a>: A Quick Note about the way I use Python: I really like [Anaconda Python Distribution](https://www.continuum.io/) or at least the [Mini Conda](http://conda.pydata.org/miniconda.html) package.  And I don't want to make `python3` as default on my machine. So ... I create an environment with `python3` by running `conda create --name <some-env-name> python=3`. Once you run `source activate <some-env-name>`, and you will find that for as long as this source is active, your default python is `py3` and default pip is `pip3`.
