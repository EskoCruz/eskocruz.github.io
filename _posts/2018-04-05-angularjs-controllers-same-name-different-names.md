---
published: true
Title: AngularJS - Use Same or Different Controller Names
layout: post
---
## How to name your controllers

Should you use the same controller name or different names. P
There is still debate on how to name your controllers.

	ng-controller="NameController as name"
vs

	ng-controller="NameController as vm"
    
    
I try to use the same name. Some think it makes the code easier to read and but I use it to try to prevent some bugs.
