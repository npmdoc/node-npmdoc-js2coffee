# npmdoc-js2coffee

#### api documentation for  [js2coffee (v2.2.0)](http://js2.coffee)  [![npm package](https://img.shields.io/npm/v/npmdoc-js2coffee.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-js2coffee) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-js2coffee.svg)](https://travis-ci.org/npmdoc/node-npmdoc-js2coffee)

#### JavaScript to CoffeeScript compiler

[![NPM](https://nodei.co/npm/js2coffee.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/js2coffee)

- [https://npmdoc.github.io/node-npmdoc-js2coffee/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-js2coffee/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-js2coffee/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-js2coffee/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-js2coffee/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-js2coffee/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Rico Sta. Cruz"
    },
    "bin": {
        "js2coffee": "./bin/js2coffee"
    },
    "browser": "js2coffee.coffee",
    "bugs": {
        "url": "https://github.com/js2coffee/js2coffee/issues"
    },
    "dependencies": {
        "escodegen": "^1.6.0",
        "esprima": "^2.5.0",
        "estraverse": "^4.1.1",
        "minimist": "^1.1.0",
        "read-input": "^0.3.1",
        "source-map": "^0.5.2"
    },
    "description": "JavaScript to CoffeeScript compiler",
    "devDependencies": {
        "browserify": "13.0.0",
        "chai": "^3.4.0",
        "coffee-script": "^1.8.0",
        "coffeeify": "^2.0.1",
        "coffeelint": "^1.6.0",
        "glob": "^7.0.0",
        "js-yaml": "^3.2.1",
        "mocha": "^2.1.0",
        "mocha-clean": "^1.0.0",
        "uglify-js": "^2.4.16",
        "underscore": "^1.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "821aaef62bbee35a29ea8c0475e20fe9f10043c5",
        "tarball": "https://registry.npmjs.org/js2coffee/-/js2coffee-2.2.0.tgz"
    },
    "gitHead": "0654118e532edcb79883aae5dd20a4a0e2e71352",
    "homepage": "http://js2.coffee",
    "keywords": [
        "javascript",
        "coffeescript",
        "language",
        "compiler"
    ],
    "license": "MIT",
    "main": "dist/js2coffee.js",
    "maintainers": [
        {
            "name": "rstacruz"
        },
        {
            "name": "balupton"
        },
        {
            "name": "timaschew"
        }
    ],
    "name": "js2coffee",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/js2coffee/js2coffee.git"
    },
    "scripts": {
        "autotest": "mocha -R min -b --watch",
        "prepublish": "mocha >/dev/null && make -B dist",
        "test": "mocha"
    },
    "version": "2.2.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
