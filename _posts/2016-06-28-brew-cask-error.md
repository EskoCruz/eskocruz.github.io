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
