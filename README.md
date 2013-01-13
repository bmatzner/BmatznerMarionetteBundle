# MarionetteJS Bundle for Symfony2

## Current Version

MarionetteJS v1.0.0-rc2

## Requirements

MarionetteJS requires Backbone and a number of dependencies included in this package.

## Installation

### Add bundle to your composer.json file

``` js
// composer.json

{
    "require": {
		// ...
        "bmatzner/marionette-bundle": "*"
    }
}
```

### Add bundle to your application kernel

``` php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Bmatzner\MarionetteBundle\BmatznerMarionetteBundle(),
        // ...
    );
}
```

### Download the bundle using Composer

``` bash
$ php composer.phar update bmatzner/marionette-bundle
```

### Install assets

Given your server's public directory is named "web", install the public vendor resources

``` bash
$ php app/console assets:install web
```

Optionally, use the --symlink attribute to create links rather than copies of the resources 

``` bash
$ php app/console assets:install --symlink web
```

## Usage

### Install and reference the dependencies for Marionette:

``` html
<script type="text/javascript" src="{{ asset('bundles/bmatznerjson2/js/json2.min.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/bmatznerjquery/js/jquery.min.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/bmatznerunderscore/js/underscore.min.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/bmatznerbackbone/js/backbone.min.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/bmatznermarionette/js/marionette.min.js') }}"></script>
```

### Install and reference the bundled Marionette package, which includes
* Backbone.EventBinder
* Backbone.BabySitter
* Backbone.Wreqr
and 
* Backbone.Marionette itself

``` html
<script type="text/javascript" src="{{ asset('bundles/bmatznermarionette/js/marionette.min.js') }}"></script>
```

Alternatively, you can load the separate packages 

``` html
<script type="text/javascript" src="{{ asset('bundles/bmatznermarionette/js/backbone.eventbinder.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/bmatznermarionette/js/backbone.babysitter.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/bmatznermarionette/js/backbone.wreqr.js') }}"></script>
<script type="text/javascript" src="{{ asset('bundles/bmatznermarionette/js/backbone.marionette.js') }}"></script>
```

## Licenses

Refer to the source code of the included files for license information

## References

1. http://marionettejs.com/
2. http://backbonejs.org/
3. http://symfony.com/
