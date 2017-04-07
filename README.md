# api documentation for  [js2coffee (v2.2.0)](http://js2.coffee)  [![npm package](https://img.shields.io/npm/v/npmdoc-js2coffee.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-js2coffee) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-js2coffee.svg)](https://travis-ci.org/npmdoc/node-npmdoc-js2coffee)
#### JavaScript to CoffeeScript compiler

[![NPM](https://nodei.co/npm/js2coffee.png?downloads=true)](https://www.npmjs.com/package/js2coffee)

[![apidoc](https://npmdoc.github.io/node-npmdoc-js2coffee/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-js2coffee_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-js2coffee/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-js2coffee/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-js2coffee/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Rico Sta. Cruz",
        "email": "hi@ricostacruz.com"
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
            "name": "rstacruz",
            "email": "rico@ricostacruz.com"
        },
        {
            "name": "balupton",
            "email": "b@lupton.cc"
        },
        {
            "name": "timaschew",
            "email": "timaschew@gmail.com"
        }
    ],
    "name": "js2coffee",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module js2coffee](#apidoc.module.js2coffee)
1.  [function <span class="apidocSignatureSpan">js2coffee.</span>build (e, t)](#apidoc.element.js2coffee.build)
1.  [function <span class="apidocSignatureSpan">js2coffee.</span>generate (e, t)](#apidoc.element.js2coffee.generate)
1.  [function <span class="apidocSignatureSpan">js2coffee.</span>parseJS (t, u)](#apidoc.element.js2coffee.parseJS)
1.  [function <span class="apidocSignatureSpan">js2coffee.</span>transform (t, u)](#apidoc.element.js2coffee.transform)
1.  string <span class="apidocSignatureSpan">js2coffee.</span>version



# <a name="apidoc.module.js2coffee"></a>[module js2coffee](#apidoc.module.js2coffee)

#### <a name="apidoc.element.js2coffee.build"></a>[function <span class="apidocSignatureSpan">js2coffee.</span>build (e, t)](#apidoc.element.js2coffee.build)
- description and source-code
```javascript
build = function (e, t){var u,n,r,i,o,a;if(t==null){t={}}if(t.filename==null){t.filename="input.js"}if(t.indent==null){t.indent=2}t.source
=e;u=s.parseJS(e,t);i=s.transform(u,t),u=i.ast,a=i.warnings;o=s.generate(u,t),n=o.code,r=o.map;return{code:n,ast:u,map:r,warnings
:a}}
```
- example usage
```shell
...
<br>

## JavaScript API

Available via npm ('require('js2coffee')'), or via CDN in the browser (as 'window.js2coffee'):

'''js
result = js2coffee.build(source);

result.code     // code string
result.ast      // transformed AST
result.map      // source map
result.warnings // array of warnings
'''
...
```

#### <a name="apidoc.element.js2coffee.generate"></a>[function <span class="apidocSignatureSpan">js2coffee.</span>generate (e, t)](#apidoc.element.js2coffee.generate)
- description and source-code
```javascript
generate = function (e, t){if(t==null){t={}}return new n(e,t).get()}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js2coffee.parseJS"></a>[function <span class="apidocSignatureSpan">js2coffee.</span>parseJS (t, u)](#apidoc.element.js2coffee.parseJS)
- description and source-code
```javascript
parseJS = function (t, u){var n,r,i;if(u==null){u={}}try{n=e("esprima");return n.parse(t,{loc:true,range:true,comment:true})}catch(i){r=i;throw
 o(r,t,u.filename)}}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js2coffee.transform"></a>[function <span class="apidocSignatureSpan">js2coffee.</span>transform (t, u)](#apidoc.element.js2coffee.transform)
- description and source-code
```javascript
transform = function (t, u){var n,r,o;if(u==null){u={}}r={};o=function(e){return i.run(t,u,e,r)};n=!(u.comments===false);if(n){o([e("./lib/transforms
/comments")])}o([e("./lib/transforms/functions")]);o([e("./lib/transforms/exponents"),e("./lib/transforms/ifs"),e("./lib/transforms
/iife"),e("./lib/transforms/literals"),e("./lib/transforms/loops"),e("./lib/transforms/members"),e("./lib/transforms/objects"),e
("./lib/transforms/binary"),e("./lib/transforms/empty_statements"),e("./lib/transforms/others"),e("./lib/transforms/precedence"),
e("./lib/transforms/returns"),e("./lib/transforms/switches"),e("./lib/transforms/unsupported")]);o([e("./lib/transforms/blocks")]);
return{ast:t,warnings:r.warnings}}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
