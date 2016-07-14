---
layout: post
title:  "Vim migrating to the habit of using an IDE"
date:   2015-04-23 00:11:50
categories: [vim, programming, code, IDE, tmux, plugins]
---

I do not plan to do a "tutorial" step by step how to migrate to VIM. On the Internet there are thousands of them in all shapes and colors.
Explaining personally as it was for me and then you try to.

I must be honest and mention of first instance which is not very easy when you already have a habit of years using a workflow to write code but the motivation to be much more productive even, finally decided to use VIM at all times and not only in the console when I access a server or edit my .zshrc.

My first steps were a bit chaotic, opened it occasionally trying to force the use and being accustomed to multiple tabs and windows with persistence that provide us with the IDE's to continue working. However in VIM he had every time I used or closing a project had to start all over again where he left off the last time you work on.

At the end I was too lazy often start from scratch and was returning to use the IDE. 
But someone came to the rescue, I remembered that for the persistence of active Shell server use TMUX and said why not use it with VIM? and got down to work, searching in the internet everyone used this perfect combination of VIM + TMUX and thereby thousand plugins and preferences for use. This changed my life. Now I could persist sessions with gem **tmuxinator** for **TMUX**  gave me the ability to create "workspaces" for each of my projects and not only with VIM, could be pre-loaded with certain **IRC** channels or whatever I wanted depending on the project that is working.

But not all end there, although now had finally stopped using my favorite IDE I felt that something was missing like tab completition, syntax highlight, browse the code, comment multiple lines fast or to see my tree directory clearly and quickly.
And there came the precious plugins to the rescue, there are thousands all over the web and well documented that solved all my shortcomings.
But then you say OK if I want to install and charge at least 20 plugins that crazy right?
Looking on how to optimize the task of installing/updating and loading plugins in VIM I found **Pathogen**, there are a lot of plugin managers some with more advantages than others but this is what my at least I settle in terms of implementation and use.

You may wonder because even not mention anything about the tediousness of having to work all the time with shortcuts keyboard since there is no mouse?
Well I wanted to leave it for last.
Once I was 100% comfortable with everything you need to use VIM I played the part of learning those keyboard shortcuts besides the classical “i” for edit “:q” for quit or “:w” for save (ah! I forgot to mention, I have a plugin that makes me autosave)
they were with those who had driven me all my life when using VIM on servers as happens to most who do not use the horrific NANO, if you're one of those, please I beg you to leave aside.

Indeed it was very simple, starting with those and slowly figuring out shortcuts see that you need them to use. Do not you become crazy learning all because it is impossible, all you get is frustrated.
A few days later you'll already feel that it is your ideal workplace and more productive.


I am a big fan of the terminal and not having to get out of there I find it incredible as it avoids distractions from other applications when changing focus, because I browse directories, get up local servers, write code and an endless number of tasks without leaving terminal. Ah! and you save RAM and CPU resources :)

Many people talk about that VIM is fantastic for its power syntax to manipulate and navigate text and this is certainly amazing but personally are many more benefits you get when you use it, you'll leave on your own to discover them.

I hope at least curiosity getting up to use VIM, I wish it so.

PS: My VIM has many installed plugins and sometimes need them on a remote server. Anyway it's completely enjoyable use the same editor anywhere you feel at home wherever you are.
Dependence is very low unless you become addicted to plugins. =P

PS2: ![](http://i.imgur.com/Fx1FXhQ.png)
