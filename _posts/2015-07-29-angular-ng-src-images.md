---
layout: post
title: Angular.js ng-src for Images
published: true
---

I am always falling victim to causing an error by using Angular Expressions inside a src attribute.

I am writing this post specifically to hopefully remember to always use ng-src.
```html
<img src="{{item.images[0].large}}" />
```

The reason for the error is the browser tries to load the image before the Expression evaluates.

The ng-src Directive is needed to print out the source.

```html
<img ng-src="{{item.images[0].large}}" />
```

Hopefully this will help with my memory.
