# grails-babel-asset-pipeline
babel.js transformation for grails-asset-pipeline

Installation
-----
add
```
compile(':babel-asset-pipeline:1.0.0')
```
to your BuildConfig.groovy's plugins block

Usage
-----
You don't have to do anything. This plugins hooks into the normal Asset-Pipeline Cycle for Javascript files and does the transformation for you.

This means you can write stuff like
```
var foo = "sparta";
console.log(`this is ${foo}`)
```
and the plugin transforms it into:
```
var foo = "sparta";
console.log("this is " + foo);
```
