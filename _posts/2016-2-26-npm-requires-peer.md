---
layout: post
title: NPM Required Peer
---

Followed by this warning:  

`UNMET PEER DEPENDENCY jshint@2.x`  
`gulp-jshint@2.0.0 requires a peer of jshint@2.x but none was installed.`

Cannot find module 'jshint/src/cli'

The gulp-jshint installation instructions show that we need jshint AND gulp-jshint in our package.json:  
`npm install jshint --save-dev`
