---
layout: post
title: Installing Homebrew on Mac
---

First thing out is going to the Apple App Store and downloading then installing XCode. Apple’s development software is used to build Mac and iOS apps. 

Next is to open up the terminal and install the Command Line Tools for Xcode.

```bash
xcode-select --install
```

You will be prompted to get the Command Line Tools for Xcode. Click Install.

Then the install of Homebrew itself. Paste this into the terminal:

```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Next, will be asked to enter your password that will give homebrew sudo (admin) access.  
You will be prompted:
```bash
==> Installation successful?
==> Next steps
Run 'brew help' to get started
```

type `brew doctor` and if everything is good it will reply:  
```bash
your system is ready to brew
```

Congrats, Homebrew Installed


####References####
Apple's XCode:
* https://itunes.apple.com/us/app/xcode/id497799835

Homebrew Sites:
* http://brew.sh
* https://github.com/Homebrew/homebrew

More references:
* http://blog.teamtreehouse.com/install-node-js-npm-mac
* https://github.com/Homebrew/homebrew/blob/master/share/doc/homebrew/Installation.md#installation
