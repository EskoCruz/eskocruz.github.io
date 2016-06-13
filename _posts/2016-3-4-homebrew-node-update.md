---
layout: post
title: Update Node with Homebrew
---

Find the version of node you currently have installed.

    $ node -v
    v5.1.0

Now I want to see what version is currently the stable version on the latest **Homebrew** repository.  
First, let us make sure we have the latest Homebrew by running the following commands.

    $ brew update
    Already up-to-date.
    $ brew doctor
    Your system is ready to brew.

Now that we are sure we are with the current Homebrew. Let's see what version of **Node** is the latest.
 
    $ brew info node
    node: stable 5.9.1 (bottled), HEAD
    Platform built on the V8 JavaScript runtime to build network applications
    https://nodejs.org/
    /usr/local/Cellar/node/4.2.1 (2,738 files, 28.6M)
      Poured from bottle
    /usr/local/Cellar/node/5.0.0 (2,824 files, 28.6M)
      Poured from bottle
    /usr/local/Cellar/node/5.1.0 (2,827 files, 28.6M) *
      Poured from bottle
    From: https://github.com/Homebrew/homebrew/blob/master/Library/Formula/node.rb
    ==> Dependencies
    Build: xz ✘, pkg-config ✘
    Optional: openssl ✘
    ==> Options
    --with-debug
    	Build with debugger hooks
    --with-full-icu
    	Build with full-icu (all locales) instead of small-icu (English only)
    --with-openssl
    	Build with openssl support
    --without-completion
    	npm bash completion will not be installed
    --without-npm
    	npm will not be installed
    --HEAD
    	Install HEAD version
    ==> Caveats
    Please note by default only English locale support is provided. If you need
    full locale support you should:
      `brew reinstall node --with-full-icu`
    
    Bash completion has been installed to:
      /usr/local/etc/bash_completion.d


On the second line, we read `node: stable 5.9.1`. We are informed that the latest stable version is 5.9.1, and we are out of date with our 5.1.0 version.

    $ brew upgrade node
    ==> Upgrading 1 outdated package, with result:
    node 5.9.1
    ==> Upgrading node
    ==> Downloading https://homebrew.bintray.com/bottles/node-5.9.1.el_capitan.bottle.tar.gz
    ######################################################################## 100.0%
    ==> Pouring node-5.9.1.el_capitan.bottle.tar.gz
    ==> Caveats
    Please note by default only English locale support is provided. If you need
    full locale support you should:
      `brew reinstall node --with-full-icu`

    Bash completion has been installed to:
      /usr/local/etc/bash_completion.d
    ==> Summary
      /usr/local/Cellar/node/5.9.1: 3,861 files, 35.6M

Done
