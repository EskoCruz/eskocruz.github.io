---
layout: post
title: Homebrew Doctor Warning
published: true
---

What to do if when you enter `brew doctor` and you get the following message:  

![brew doctor warning]({{site.baseurl}}/_posts/brew-doctor-warning.png)

```
**Please note that these warnings are just used to help the Homebrew maintainers
with debugging if you file an issue. If everything you use Homebrew for is
working fine: please don't worry and just ignore them. Thanks!**

_Warning:_ Some directories in /usr/local/share/man aren't writable.
This can happen if you "sudo make install" software that isn't managed
by Homebrew. If a brew tries to add locale information to one of these
directories, then the install will fail during the link step.

You should probably `sudo chown -R $(whoami)` them:  
`    /usr/local/share/man/man8`
```
------------------------------

1. `chown` is the unix command to change the ownership of a file.  
Homebrew is asking to change the ownership of `/usr/local/share/man/man8` so that Homebrew can write to it. Homebrew runs with the same permissions as I do, so making myself the file's owner should solve the problem.

2. Running this command will correct this problem and the warning will go away.  
`sudo chown -R $(whoami) /usr/local/share/man/man8`

3. Now it will prompt for your password.  
`Password:`

4. After your password is entered correctly run `brew doctor` again. Now you should finally get `Your system is ready to brew.`
