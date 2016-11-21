---
published: true
title: What does (!) next to a cask mean
layout: post
---
![Exclamation mark next to cask name]({{ site.baseurl }}/images/exclamation-mark-cask-name.png "Brew cask name with exclamation mark")  

When I used last used `brew cask list`, I noticed that one cask names had an exclamation mark next to it: `(!)`

It means the cask no longer exists. You installed it when it did. Search for it now, and it won’t find it.
 
Best is to remove all files associated with the given cask. We do this by invoking the brew zap command `brew cask zap <cask-name>`. From here you can install brew cask you want if it was renamed if it is still part of the brew cask.