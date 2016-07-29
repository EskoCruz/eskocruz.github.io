---
published: true
title: Brew Cask Update Not Moving or Overwriting
layout: post
---

When I run 'brew cask install iterm2'

```
==> Downloading https://iterm2.com/downloads/stable/iTerm2-3_0_5.zip
######################################################################## 100.0%
==> Verifying checksum for Cask iterm2
==> It seems there is already an App at '/Applications/iTerm.app'; not moving.
```

How to resolve this conflict of iTerm not updating?

Run it with `--force`.

`brew cask install iterm2 --force`

```
==> Satisfying dependencies
complete
==> Downloading https://iterm2.com/downloads/stable/iTerm2-3_0_5.zip
######################################################################## 100.0%
==> Verifying checksum for Cask iterm2
==> It seems there is already an App at '/Applications/iTerm.app'; overwriting.
==> Removing App: '/Applications/iTerm.app'
==> Moving App 'iTerm.app' to '/Applications/iTerm.app'
🍺  iterm2 was successfully installed!
```

If installed with `--force`, the behavior is to overwrite the existing one.

NOTE: If this is a case of MAS (Mac App Store) install, then removing the existing one and installing again will fix it.