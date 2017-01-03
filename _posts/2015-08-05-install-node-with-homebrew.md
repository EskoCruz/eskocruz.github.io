---
layout: post
title: Installing Node.js on Mac with Homebrew
published: true
---

This is going to be short and sweet because the real work already went into installing Homebrew onto the mac. Documented here on my previous post: [Installing Homebrew on Mac](http://eskocruz.github.io/install-homebrew/)

The entire reason for installing Homebrew is for making installations like these as painless as possible. Homebrew handles downloading, unpacking and installing Node and NPM on your system.  
Lets get started by opening our terminal.  
Type the following brew command:  
```
brew install node
```
Just wait and you will see that the "Caveats" being installed and extracting 'node' onto a folder they interestingly named "Cellar" /usr/local/Cellar/node/__latest_version-number__.

just to verify like we did with installing Homebrew, lets run a couple simple commands to see the versions of Node and NPM installed:  
To see if Node is installed, type the following into the Terminal
```
node -v
```
This should print the version number so you’ll see something like this 
```
v0.12.7.
```
To see if NPM is installed, type the following into the Terminal:
```
npm -v
```
This should print the version number so you’ll see something like this 
```
2.12.1
```
Done, Installed and Verified!
