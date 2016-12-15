---
layout: post
title: Ember CLI and Watchman
published: true
---
When Watchman is not installed, a notice is displayed when invoking various commands. You can safely ignore this message:

    $ ember version
    Could not start watchman; falling back to NodeWatcher for file system events.
    Visit http://ember-cli.com/user-guide/#watchman for more info.

Here is what **Watchman** is and why you should not ignore this message.

## What is Watchman? ##
Watchman is a simple utility to watch files/directories and perform an action when they change.
Watchman provides Ember CLI a more effective way for watching project changes. On OSX and UNIX-like operating systems, **Ember** recommend installing Watchman version 3.x.

## Why not let Ember CLI fallback to NodeWatcher? ##
File-watching on OSX is error-prone and Node’s built-in NodeWatcher has trouble observing large trees. Watchman on the other hand, solves these problems and performs well on extremely massive file trees.

## How do I use Watchman instead of NodeWatcher? ##
On OSX, you can install Watchman using Homebrew:

    $ brew install watchman
