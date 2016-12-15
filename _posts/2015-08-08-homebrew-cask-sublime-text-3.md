---
layout: post
title: 'To install, drag this icon no more!'
published: true
---

Homebrew Cask extends Homebrew and brings its elegance, simplicity, and speed to OS X applications and large binaries alike.

I came across Homebrew Cask because I wanted to start using Sublime Text 3. For that I needed to uninstall Sublime Text 2. To do that all I could find to do was to take the icon and drag it into the trash can. I do not know how thuo this process is or even understood the installing process of dragging the icon into the Application folder. I started thinking if there was a way that I could install these programs like I do tools using Homebrew that also has the benefit of allowing me to uninstall these programs in an easy one line uninstall command.

Thank you internet, people were already way ahead of me. I came across "Homebrew Cask". To install this all I had to do was enter in my Terminal:
```bash
$ brew install caskroom/cask/brew-cask
```
Before installing anything with brew, make sure its up to date. In the Terminal type:
```bash
$ brew update
```
Then type:
```bash
$ brew doctor
```
if everything is good it will print out the following message:
```bash
> Your system is ready to brew.
```
Now with Homebrew Cask installed you can now quickly in command line install programs like Google Chrome.
```bash
$ brew cask install google-chrome
==> Downloading https://dl.google.com/chrome/mac/stable/GGRO/googlechrome.dmg
==> Success! google-chrome installed to /opt/homebrew-cask/Caskroom/google-chrome/stable-channel
==> Linking Google Chrome.app to /Users/username/Applications/Google Chrome.app
```
Best part is now I can easy uninstall in my wished for one line command:
```bash
$ brew cask uninstall google-chrome
```
Now the time has finally come to install Sublime Text 3
```bash
$ brew tap caskroom/versions
$ brew cask install sublime-text3
```


####Resources:####
* http://caskroom.io/
* https://github.com/caskroom/homebrew-cask
* https://github.com/caskroom/homebrew-cask/blob/master/USAGE.md
