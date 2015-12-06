[![Build Status](https://travis-ci.org/errbuddy/babel-asset-pipeline.svg?branch=master)](https://travis-ci.org/errbuddy/babel-asset-pipeline)

# grails-babel-asset-pipeline
babel.js transformation for grails-asset-pipeline

# Installation
-----
add
```
compile(':babel-asset-pipeline:1.4.2')
```
to your BuildConfig.groovy's plugins block

-----

# Configuration
```
grails.assets.babel.enabled = true // boolean 
```
default to true.

```
grails.assets.babel.processJsFiles = false // boolean
```
defaults to false. Whether to process JsAssetFiles (.js) too. **By default to Processor only touches Es6AssetFiles (.es6)!**

```
grails.assets.babel.options = [blacklist: ['useStrict'], loose: 'all'] // babel transfom options. see https://babeljs.io/docs/usage/options/ for more information
```
defaults to null. A Map of options passed to babels transform method. see https://babeljs.io/docs/usage/options/ for possible values

## Modules
```
grails.asset.babel.options = [modules: 'amd', moduleIds: true]
```
When the `moduleIds` option is set the plugin provides Babel with a `moduleId` for each file. The ID is the relative path of the file inside `grails-app/assets/javascripts` with the file extension removed. 

```
e.g.
# File Path:
grails-app/assets/javascripts/foo/bar.js
# Generated moduleId:
foo/bar
```

Note: Explicit module IDs are not available when generating CommonJS modules.
