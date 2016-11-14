---
published: true
title: Brew Doctor Symlinks Prune
layout: post
---

After running a `brew update`, it is best to next run `brew doctor`. Sometimes you may run into broken symlinks message like after an operating system or xcode update for example.

```
$ brew doctor
```
```
Please note that these warnings are just used to help the Homebrew maintainers
with debugging if you file an issue. If everything you use Homebrew for is
working fine: please don't worry and just ignore them. Thanks!

Warning: Broken symlinks were found. Remove them with `brew prune`:
  /usr/local/bin/csslint
  /usr/local/lib/node_modules/yo/node_modules/.bin/fullname
  /usr/local/lib/node_modules/yo/node_modules/.bin/opn
  /usr/local/lib/node_modules/yo/node_modules/.bin/repeating
  /usr/local/lib/node_modules/yo/node_modules/.bin/user-home
  /usr/local/lib/node_modules/yo/node_modules/yeoman-character/node_modules/.bin/supports-color
  /usr/local/share/man/man8/prlexec.8
  
```
```
$ brew prune
```
```
Error: Permission denied - /usr/local/share/man/man8/prlexec.8
```
```
$ brew doctor
```
```
Please note that these warnings are just used to help the Homebrew maintainers
with debugging if you file an issue. If everything you use Homebrew for is
working fine: please don't worry and just ignore them. Thanks!

Warning: Broken symlinks were found. Remove them with `brew prune`:
  /usr/local/share/man/man8/prlexec.8
```  
As mentioned in my post [Homebrew Doctor Warning](http://eskocruz.github.io/homebrew-doctor-warning/), running this command will correct this problem and the warning will go away.  
`sudo chown -R $(whoami) /usr/local/share/man/man8`  

Now rerun `brew prune`.
```
$ brew prune
Pruned 1 symbolic links and 1 directories from /usr/local
```

After your password is entered correctly run `brew doctor` again. Now you should finally get: `Your system is ready to brew.`