---
layout: post
title: Running Git through Homebrew instead of XCode
published: true
---

You are setting up your DEV environment. You setup Homebrew on your machine to so you can install node.js, GIT, and alike. Problem is that to install Homebrew, you needed to install XCode. XCode installs a version of GIT onto your mac automatically to use for Xcode development so when you input `which git` the directory points to `/usr/bin/git`. `git --version` prints `git version 2.3.2 (Apple Git-55)` when the latest is already GIT 2.5.0

Here is the catch 22 I ran into.  
Do i need to modify and update the Xcode GIT? Do I install GIT through Homebrew and then modify that GIT settings so it doesn't relate to the Xcode GIT? Or do I need to go to https://git-scm.com/ and install the latest GIT and modify that?

Last thing I wanna do is install incorrectly and possibly ruin/corrupt my environment so far in. I took me a while and a lot of research because there are so many postings about this problem and to correct this problem but hardly any explaining what they did/install to get this problem, but worst of all, what is the best to setup GIT especially if you have Homebrew with Xcode already installed.

Now lets get the party started.
```
$ brew install git
------------------
==> Summary
 /usr/local/Cellar/git/2.5.0: 1383 files, 32M
```
Now lets check the GIT version.
```
$ git --version
git version 2.5.0
```
```
$ which git
/usr/local/bin/git
```
There was no worry! Old postings are wrong and looks like this is no longer an issue!.

Resource:
http://apple.stackexchange.com/questions/144871/updating-and-running-git-through-homebrew-instead-of-xcode
