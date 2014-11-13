# Sinon #555

This is a reduced test case to show [Sinon issue #555](https://github.com/cjohansen/Sinon.JS/issues/555) in action.

The core of the issue is that you cannot load a built version of SinonJS with RequireJS (or other AMD loaders).

Since the [website](http://sinonjs.org) encourages people to download a built version, having it work with RequireJS is probably not an unreasonable expectation.


## Steps to reproduce

```
$ npm install
$ python -m SimpleHTTPServer 8421
```

Go to [http://localhost:8421/load-with-requirejs.html](http://localhost:8421/load-with-requirejs.html), observe the console, there will be errors from RequireJS.

For completeness, loading built SinonJS via a script tag still works: [http://localhost:8421/load-with-scripttag.html](http://localhost:8421/load-with-scripttag.html) 