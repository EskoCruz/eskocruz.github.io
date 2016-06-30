---
published: true
title: Brew cask upgrade error
post: null
layout: post
---

When trying to update brew cask with the following command:  
`brew upgrade brew-cask`  

Did you ever get the following error?  
`Error: caskroom/cask/brew-cask not installed`

The reason for this error:
    Warning: The default Caskroom location has moved to /usr/local/Caskroom.

    Please migrate your Casks to the new location and delete /opt/homebrew-cask/Caskroom,
    or if you would like to keep your Caskroom at /opt/homebrew-cask/Caskroom, add the
    following to your HOMEBREW_CASK_OPTS:

      --caskroom=/opt/homebrew-cask/Caskroom

    For more details on each of those options, see https://github.com/caskroom/homebrew-cask/issues/21913.
    Error: This command requires a Cask token
    
Easiest way is to move with the following comand: `mv /opt/homebrew-cask/Caskroom /usr/local`.  

Casks installed prior to september 2015 will need to be re-installed manually because they were symlinked rather than moved to their destinations.

`brew-cask` is no longer under `brew list`. So `brew upgrade brew-cask` will no longer work and give you the error `Error: caskroom/cask/brew-cask not installed`. But don't worry. It's now implemented as a homebrew [external command](https://github.com/Homebrew/brew/blob/master/share/doc/homebrew/External-Commands.md) called cask.

### Resource
[https://github.com/caskroom/homebrew-cask](https://github.com/caskroom/homebrew-cask)
