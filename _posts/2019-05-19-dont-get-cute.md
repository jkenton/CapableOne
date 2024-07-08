---
layout: post
title:  "Don't get too cute"
date:   2019-05-19 12:00:00 -0400
categories: emacs nerdery thinking
---



I thought I could share the .emacs.d/ folder (using Dropbox) from one installation to another... Nope.

The .emacs.d/folder contains not just definitions of modules or packaages installed, but also compiled programs. That means, each emacs.d/ folder is kinda machine/installation specific.
#+HTML: <!--more-->
I /did/ learn some valuable shortcuts:

1. Leave the .emacs file in the Dropbox folder, and create a symlink to it from each installation
2. Create a symlink to the folder that contains the .org files (including the org2blog files) on each installation
3. Use the package manager ~M-x install-package~ to install
4. org2blog
5. ox-hugo (required for the Hydra to work)

It works really well! Smooth!
