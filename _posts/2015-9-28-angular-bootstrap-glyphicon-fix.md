---
layout: post
title: Angular Bootstrap Glyphicon Fix
---

In the bower.json file add:  
	
```json
	"overrides": {
		"bootstrap-sass-official": {
			"main": [
				"assets/stylesheets/_bootstrap.scss",
				"assets/fonts/bootstrap/glyphicons-halflings-regular.eot",
				"assets/fonts/bootstrap/glyphicons-halflings-regular.svg",
				"assets/fonts/bootstrap/glyphicons-halflings-regular.ttf",
				"assets/fonts/bootstrap/glyphicons-halflings-regular.woff",
				"assets/fonts/bootstrap/glyphicons-halflings-regular.woff2"
			]
		}
	}
```
