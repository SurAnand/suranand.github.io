---
layout: post
title: Just One Simple Error - GitHub Page Build Fails
comments: true
---

![alt text](http://timjames.me/img/jekyll/feature.jpg "https://jekyllrb.com/")

### This is all about a tiny tiny error I made in organizing my github pages repo locally and everything ended up going wrong. Finally, my GitHub pages site, this site, would not get any of my new posts.

This killed almost over 3 hours of my time. I still wanted to keep an update here, so if ever I make similar mistakes, I could check this post, like making my head-banging process manageable.

## Here is the story!

I have been maintaining this site, although not as seriously. At least, whenever I feel there is something worth noting down, I would immediately start scribbling my story in markdown syntax using `vi` and then use `pandoc` and `lynx` for previwing my `.md` file within terminal. This markdown-preview within terminal is one of my recent discoveries. I am thankful to the makers for helping me stick on to terminal for all things once considered only browser-based. 

### Here is how I do `markdown-preview` from within my Terminal

As per the makers' suggestion, I just needed to add these lines to my `.profile` file.

```
### Preview Markdown files from within Terminal. 
### Source of this info: http://tosbourn.com/view-markdown-files-terminal/
### This makes use of Pandoc & Lynx
### Note: This LYNX thing shocked me like crazy. Linux is an art, really!!!
rmd() {
        pandoc $1 | lynx -stdin
}
```

This is it! The colors and format appears in `lynx` style and I find it really very cool.

### Back to the Story

I got an idea. I wanted to keep a directory within my GitHub pages repo, called `drafts` which should contain my writing-in-progress files.

And to make things easier (and to prove that I am lazier than ever), I added the usual [Poole-Jekyll](https://github.com/poole/poole) specific config lines at the beginning of the post. Something like this:

```
---
layout: post
title: Just One Simple Error - GitHub Page Build Fails
comments: true
---
```

And then pushed all my new stuff into the remote.

> Bang!

I hit the wall. The GitHub won't build my pages. It sent me a very generic email that said,

> Page build failed. For more information, see https://help.github.com/articles/troubleshooting-github-pages-build-failures.

And I went all over the cosmos of *google* trying to find the god who can help me with this.

First I thought, it was because of my email on GitHub being verified, following the suggestions on GitHub help pages. That didn't help. Then, I thought it was due to my global config settings of my git on my machine and tried to reconfigure all of it. Nope, that wasn't the issue too. And then I remembered I formatted my OS about a month ago which might have resulted in Jekyll-build related issues. So I started working around installing `Jekyll` which required `gem`, which again required `ruby`, which further needs `rvm` to be installed on my machine.

Honestly, anything that has to do with either of **Java, JavaScript and Ruby**, I just cannot find myself having sufficient patience. It always turned into a nightmare everytime I tried to get these things to work on my machine. I wish somebody like [Digital Ocean](https://cloud.digitalocean.com/) writes a simple and easy-to-follow instructions on how to work on this stuff. 

Anyway, I somehow managed to get all this worked out and made my system ready with all these pre-requisites. I still cannot see my GitHub page updated with my new post. I could not undestand what else to do now. And then I tried `jekyll build` and `jekyll serve` inside my site directory. Both of them gave me a common error.

```
Deprecation: You appear to have pagination turned on, but you haven't included the `jekyll-paginate` gem. Ensure you have `gems: [jekyll-paginate]` in your configuration file.
```

I started searching for this stuff now. Somebody asked me to make use of `gem:jekyll-paginate` plugin and include this in the `_config.yml` of my jekyll site. I did that after installing jekyll-paginate gem. I could get rid of the error above. But I still continued getting one more error.

```
Invalid Date: '' is not a valid datetime.
  Liquid Exception: exit in _layouts/post.html
```

This became totally impossible to find where it all went wrong. Purely by chance, I came across a forum discussion where one of the responders asked a [question](https://github.com/jekyll/jekyll/issues/2003).

> Are you trying to use `layout: post` for something other than a post?

That triggered my brain!

Remember, I mentioned about my directory creation inside my site repo, `drafts` and I added the `layout: post` entry in my post? I went back to that file, deleted it and pushed into the remote.

That's it! This is all that went wrong. Even if I minus all my efforts in installing `jekyll & ruby`, finding this simple mistake became an impossible task. It finally worked! And here I am, back to my scirbbling!

Hope it helps others, especially, someone like me!
