---
published: false
title: Linters with Sublime
---
A linter is a small program that checks code for stylistic or programming errors. Linters are available for most syntaxes. The advantage of using SublimeLinter is that your code can be linted **as you type** (before saving your changes) and any errors are highlighted **immediately**, which is considerably easier than saving the file, switching to a terminal, running a linter, reading through a list of errors, then switching back to Sublime Text to locate the errors!

SublimeLinter itself is only a **framework** for linters. Linter plugins are  not  part of SublimeLinter 3.

## Installing SublimeLinter

Follow "Installing Plugins via Package Control" derections in my other post and when the list of available packages appears, type `linter` and select `SublimeLinter`.

**Note:** The github repository name is “SublimeLinter3”, but the plugin name remains “SublimeLinter”.

## Installing SublimeLinter Plugins

SublimeLinter 3 must be installed in order to use this plugin and other linters.

### SublimeLinter-jshint

This linter plugin for SublimeLinter provides an interface to JSHint. It will be used with files that have the “JavaScript” syntax, or within `<script>` tags in HTML files.

Before installing this plugin, you must ensure that `jshint` is installed on your system. To install `jshint`, do the following:
1. Install [Node.js](https://nodejs.org/en/).
2. Install `jshint` by typing the following in a terminal:
    npm install -g jshint
3. Follow "Installing Plugins via Package Control" derections above and when the plugin list appears, type `jshint`. Among the entries you should see `SublimeLinter-jshint`. If that entry is not highlighted, use the keyboard or mouse to select it.  
**Warning:** Do NOT install jshint. Install SublimeLinter-jshint.


### SublimeLinter-csslint

This linter plugin for SublimeLinter provides an interface to `CSS Lint`. It will be used with files that have the “CSS” syntax, or within `<style>` tags in HTML files.

Before installing this plugin, you must ensure that `csslint` is installed on your system. To install `csslint`, do the following:
1. Install [Node.js](https://nodejs.org/en/).
2. Install `csslint` by typing the following in a terminal:
    npm install -g csslint
3. Follow "Installing Plugins via Package Control" derections above and when the plugin list appears, type `csslint`. Among the entries you should see `SublimeLinter-csslint`. If that entry is not highlighted, use the keyboard or mouse to select it.
