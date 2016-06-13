---
layout: post
title: 'Brew Error "Warning: Broken symlinks were found."'
---

If you try `brew doctor` and you get the following error:

```
$ brew doctor  
lease note that these warnings are just used to help the Homebrew maintainers  
with debugging if you file an issue. If everything you use Homebrew for is  
working fine: please don't worry and just ignore them. Thanks!
  
Warning: Broken symlinks were found. Remove them with 'brew prune':    

  /usr/local/lib/node_modules/yo/node_modules/.bin/latest-version  
```

just use `brew prune` and the error will be fixed.

```
$ brew prune  
  Pruned 1 symbolic links and 6 directories from /usr/local
```
```
$ brew doctor  
Your system is ready to brew.
```  
