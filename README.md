# grails-babel-asset-pipeline
babel.js transformation for grails-asset-pipeline

# Installation
-----
add
```
compile(':babel-asset-pipeline:1.3.1')
```
to your BuildConfig.groovy's plugins block

-----

# Configuration
```
grails.assets.babel.enabled = true // boolean 
```
default to true. enables the plugin

```
grails.assets.babel.processJsFiles = false // boolean
```
defaults to false. Whether to process JsAssetFiles (.js) too. **By default to Processor only touches Es6AssetFiles (.es6)!**

```
grails.assets.babel.options = [blacklist: ['useStrict'], loose: 'all'] // babel transfom options. see https://babeljs.io/docs/usage/options/ for more information
```
defaults to null. A Map of options passed to babels transform method. see https://babeljs.io/docs/usage/options/ for possible values

