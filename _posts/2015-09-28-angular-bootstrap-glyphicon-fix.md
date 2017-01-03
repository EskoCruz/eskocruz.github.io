---
layout: post
title: Angular Bootstrap Glyphicon Fix
published: true
---

In the bower.json file add:  
	
```json
	"overrides": {
		"bootstrap-sass": {
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

In the `src/app/index.scss` don't forget to change the `$icon-font-path` variable from  
`../../bootstrap-sass/assets/fonts/bootstrap/`  
and add in `bower_components` to look like the following  
`$icon-font-path: "../../bower_components/bootstrap-sass/assets/fonts/bootstrap/";`
