---
layout: post
title: Just Learned VIM in 10 min
comments: true
---

![alt text](http://www.ibm.com/developerworks/aix/library/au-speakingunix_vim/04_vim.jpg "VIM")

> On the offset, I wrote this post in VIM. Thanks to **[Henrik Huttunen](http://personal.inet.fi/koti/egaga/)** for this new skill of mine.

As part of making-myself process, one of the most brilliant things I have ever come across in my life is this  [VIM Tutorial](http://openvim.com/). I truly feel enlightened to think that there are so many people out there who just create things not just for the heck of doing it, but rather to help a bunch of unknown friends in this world. Their outreach is so overarching that I wonder what gives them this kind of problem-solving attitude and a heart of contributing to the world voluntarily, with no expectations whatsoever. Is this is a phenomenon hardwired in their minds, a DNA transmitted from generations or their experiences that drive them to ideas like this.

One of the lessons in this tutorial talks about two shortcut keys in ***VIM editor***:
* `'o'` which inserts a line and puts you in `--INSERT--` mode enabling you to write the content.
* `'O'` which does the same thing but inserting a line before your current position.

And the lesson ends with a line that says,
> I bet you feel like `O_ _ _o`

And I truly felt that.

Other truly _interactive_ lessons include:

### 1. VIM - 3 Incarnations:
  * VIM's `Normal` mode: Lets you use all the VIM commands/shortcuts.
  * VIM's `--INSERT--` mode: Lets you write and edit content.
  * VIM's `--VISUAL--` mode: Lets you select text and manipulate.

### 2. Write (edit), Conquer (save) & Go (quit):
  * Type `:w` to save the work.
  * Type `:q` to quit VIM after saving.
  * Type `:q!` to quit without saving.
  * Type `:wq` to save and quit.
  * Add `!` to force these commands.

### 3. Plucking out the arrow keys on your keyboard:
  * Moving your cursor in normal mode:
    * `h` for moving left
    * `l` for moving right
    * `j` for moving down
    * `k` for moving up

### 4. Letters speak louder than Words:
  * Moving within your words in normal mode:
    * `w` for the first letter of the next Word
    * `b` for the beginning of the word
    * `e` for the end of the word

### 5. A Shocking Movement: w/ Numbers & Symbols
  * Numbers in VIM's normal mode have additional meanings:
    * Typing `9w` is pressing `w` _nine_ times.
    * `6l` is pressing `l` _six_ times.
    * `5iAnand` inserts my name `Anand` _five_ times.
    * `%` takes you to parenthesis.
    * `0` and `$` take you to the beginning and the end of a line, respectively.
    * `gg` takes you to the beginning of the file.
    * `G` takes you to the end of the file.
    * And `7G` takes you to the line-7 in the file.

> And a lot more like this. I think with this much, I am on the go!

***For the entire power of VIM, here is an entire [VIM Cheat Sheet](http://www.cse.iitk.ac.in/users/bms/pdfDoc/UnixviHelp.pdf).***

I am not sure if I am going lost in an unfamiliar world of this kind of people full of activity, ideas and innovation. Or I perhaps have the weakness of despairing so much about myself when I encounter new knowledge that I get into this emotional roller-coaster.

But the fact is, these people remind me of how late I am and how much time I irrevocably left unused and unnoticed in my life. Despite the fact that these feelings are harder and deeper in my mind than the thoughts that would motivate me to just kick-restart my life all over again, I keep telling myself, **Better late than never!**

I strongly recommend all those school students who never had the privilege of playing with computers to go to this [OpenVIM site](http://openvim.com/) and play around a bit with **Writing content and editing it on just one window.** Why, just do your homework in VIM and _"dumbstrike"_ your teachers ;-).

I am sure this will take you to spaces and times where you will surely thank this guy and think of writing some code for scientific computing and hi-fi simulation tasks. Not only that, visiting this kind of websites nurture and nourish your minds and lead you to the ideas never imagines and thoughts of living in this beautiful wonderland of truly **Open Source World**.
