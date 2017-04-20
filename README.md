# npmdoc-array-flatten

#### api documentation for  [array-flatten (v2.1.1)](https://github.com/blakeembrey/array-flatten)  [![npm package](https://img.shields.io/npm/v/npmdoc-array-flatten.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-array-flatten) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-array-flatten.svg)](https://travis-ci.org/npmdoc/node-npmdoc-array-flatten)

#### Flatten nested arrays

[![NPM](https://nodei.co/npm/array-flatten.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/array-flatten)

- [https://npmdoc.github.io/node-npmdoc-array-flatten/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-array-flatten/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-array-flatten/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-array-flatten/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-array-flatten/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-array-flatten/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "array-flatten",
    "version": "2.1.1",
    "description": "Flatten nested arrays",
    "main": "array-flatten.js",
    "typings": "array-flatten.d.ts",
    "files": [
        "array-flatten.js",
        "array-flatten.d.ts",
        "LICENSE"
    ],
    "scripts": {
        "lint": "standard",
        "test-spec": "mocha -R spec --bail",
        "test-cov": "istanbul cover node_modules/mocha/bin/_mocha -- -R spec --bail",
        "test": "npm run lint && npm run test-cov",
        "benchmark": "node benchmark"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/blakeembrey/array-flatten.git"
    },
    "keywords": [
        "array",
        "flatten",
        "arguments",
        "depth",
        "fast",
        "for"
    ],
    "author": {
        "name": "Blake Embrey",
        "url": "http://blakeembrey.me"
    },
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/blakeembrey/array-flatten/issues"
    },
    "homepage": "https://github.com/blakeembrey/array-flatten",
    "devDependencies": {
        "benchmarked": "^0.2.5",
        "istanbul": "^0.4.0",
        "mocha": "^3.1.2",
        "standard": "^8.5.0"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
