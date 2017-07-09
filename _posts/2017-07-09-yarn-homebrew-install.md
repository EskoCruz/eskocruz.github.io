---
published: true
title: Installing Yarn through Homebrew
---
You can install Yarn through the Homebrew package manager. This will also install Node.js if it is not already installed.

	brew install yarn  

If you use nvm you should exclude installing Node.js so that nvm’s version of Node.js is used.  

	brew install yarn --ignore-dependencies

NOTE: Must restart termial before yarn command will work
to verify yarn install, after restarting terminal:

	yarn --version  


[Yarn](https://yarnpkg.com). Yet Another Resource Negotiator.

[Yarn: node special dependency #1408](https://github.com/Homebrew/brew/pull/1408) Exlude Node.js?  

