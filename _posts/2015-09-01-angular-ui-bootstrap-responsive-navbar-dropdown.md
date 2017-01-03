---
layout: post
title: AngularUI Bootstrap Navbar Dropdown Fix
published: true
---

AngularUI Bootstrap Responsive Navbar Dropdown
Responsive dropdown navbar with angular-ui bootstrap
Angular UI Bootstrap 

```html
<nav class="navbar navbar-static-top navbar-inverse">
  <div class="container-fluid">
    <div class="navbar-header">
      <a class="navbar-brand" href="https://github.com/Swiip/generator-gulp-angular">
        <span class="glyphicon glyphicon-home"></span> Gulp Angular
      </a>
    </div>

    <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-6">
      <ul class="nav navbar-nav">
        <li class="active"><a ng-href="#">Home</a></li>
        <li><a ng-href="#">About</a></li>
        <li><a ng-href="#">Contact</a></li>
      </ul>

    </div>
  </div>
</nav>
```

``` html
<nav class="navbar navbar-static-top navbar-inverse">
	<div class="container-fluid">
		<div class="navbar-header">
			<button type="button" class="navbar-toggle" ng-init="navCollapsed = true" ng-click="navCollapsed = !navCollapsed" data-toggle="collapse" data-target=".navbar-collapse">
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
			</button>
			<a class="navbar-brand" href="https://github.com/Swiip/generator-gulp-angular">
				<span class="glyphicon glyphicon-home"></span> Gulp Angular
			</a>
		</div>

		<div class="collapse navbar-collapse" id="bs-example-navbar-collapse-6" ng-class="{'in': !navCollapsed}">
			<ul class="nav navbar-nav">
				<li class="active"><a ng-href="#">Home</a></li>
				<li><a ng-href="#">About</a></li>
				<li><a ng-href="#">Contact</a></li>
			</ul>
		</div>
	</div>
</nav>
<div ng-controller="ShellCtrl as vm">
	<div id="adminNavBar" class="navbar navbar-default navbar-fixed-top">
		<div class="container-fluid">
			<div class="navbar-header">
				<button type="button" class="navbar-toggle" ng-init="navCollapsed = true" ng-click="navCollapsed = !navCollapsed" data-toggle="collapse" data-target=".navbar-collapse">
					<span class="icon-bar"></span>
					<span class="icon-bar"></span>
					<span class="icon-bar"></span>
				</button>
				<a class="navbar-brand" href="/">
					<i class="icon-home"></i>
					<span>Sports Schedule Admin</span>
				</a>
			</div>
			<div class="collapse navbar-collapse" ng-class="{'in': !navCollapsed}">
				<ul class="nav navbar-nav">
					<li><a data-toggle="collapse" data-target=".navbar-collapse" href="#/">Home</a></li>
					<li><a data-toggle="collapse" data-target=".navbar-collapse" href="#/leagues">Leagues</a></li>
					<li><a data-toggle="collapse" data-target=".navbar-collapse" href="#/locations">Locations</a></li>
				</ul>
			</div>

		</div>
	</div>

	<div ng-show="vm.showSpinner" class="page-splash dissolve-animation">
		<div data-spinner="vm.spinnerOptions"></div>
		<div class="page-splash-message page-splash-message-subtle">{{vm.spinnerMessage}}</div>
	</div>

	<div ng-view id="ng-view" class="container slide-animation admin-content"></div>

</div>
```


https://angular-ui.github.io/bootstrap/
