# api documentation for  [array-flatten (v2.1.1)](https://github.com/blakeembrey/array-flatten)  [![npm package](https://img.shields.io/npm/v/npmdoc-array-flatten.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-array-flatten) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-array-flatten.svg)](https://travis-ci.org/npmdoc/node-npmdoc-array-flatten)
#### Flatten nested arrays

[![NPM](https://nodei.co/npm/array-flatten.png?downloads=true)](https://www.npmjs.com/package/array-flatten)

[![apidoc](https://npmdoc.github.io/node-npmdoc-array-flatten/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-array-flatten%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-array-flatten/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-array-flatten/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-array-flatten/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Blake Embrey",
        "email": "hello@blakeembrey.com",
        "url": "http://blakeembrey.me"
    },
    "bugs": {
        "url": "https://github.com/blakeembrey/array-flatten/issues"
    },
    "dependencies": {},
    "description": "Flatten nested arrays",
    "devDependencies": {
        "benchmarked": "^0.2.5",
        "istanbul": "^0.4.0",
        "mocha": "^3.1.2",
        "standard": "^8.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "426bb9da84090c1838d812c8150af20a8331e296",
        "tarball": "https://registry.npmjs.org/array-flatten/-/array-flatten-2.1.1.tgz"
    },
    "files": [
        "array-flatten.js",
        "array-flatten.d.ts",
        "LICENSE"
    ],
    "gitHead": "b5619025bfb5d624fc2106ec81f9fdecf5419e04",
    "homepage": "https://github.com/blakeembrey/array-flatten",
    "keywords": [
        "array",
        "flatten",
        "arguments",
        "depth",
        "fast",
        "for"
    ],
    "license": "MIT",
    "main": "array-flatten.js",
    "maintainers": [
        {
            "name": "blakeembrey",
            "email": "hello@blakeembrey.com"
        }
    ],
    "name": "array-flatten",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/blakeembrey/array-flatten.git"
    },
    "scripts": {
        "benchmark": "node benchmark",
        "lint": "standard",
        "test": "npm run lint && npm run test-cov",
        "test-cov": "istanbul cover node_modules/mocha/bin/_mocha -- -R spec --bail",
        "test-spec": "mocha -R spec --bail"
    },
    "typings": "array-flatten.d.ts",
    "version": "2.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module array-flatten](#apidoc.module.array-flatten)
1.  [function <span class="apidocSignatureSpan">array-flatten.</span>depth (array, depth)](#apidoc.element.array-flatten.depth)
1.  [function <span class="apidocSignatureSpan">array-flatten.</span>from (array)](#apidoc.element.array-flatten.from)
1.  [function <span class="apidocSignatureSpan">array-flatten.</span>fromDepth (array, depth)](#apidoc.element.array-flatten.fromDepth)



# <a name="apidoc.module.array-flatten"></a>[module array-flatten](#apidoc.module.array-flatten)

#### <a name="apidoc.element.array-flatten.depth"></a>[function <span class="apidocSignatureSpan">array-flatten.</span>depth (array, depth)](#apidoc.element.array-flatten.depth)
- description and source-code
```javascript
function flattenDepth(array, depth) {
  if (!Array.isArray(array)) {
    throw new TypeError('Expected value to be an array')
  }

  return flattenFromDepth(array, depth)
}
```
- example usage
```shell
...

'''javascript
var flatten = require('array-flatten')

flatten([1, [2, [3, [4, [5], 6], 7], 8], 9])
//=> [1, 2, 3, 4, 5, 6, 7, 8, 9]

flatten.depth([1, [2, [3, [4, [5], 6], 7], 8], 9], 2)
//=> [1, 2, 3, [4, [5], 6], 7, 8, 9]

(function () {
  flatten.from(arguments) //=> [1, 2, 3]
})(1, [2, 3])
'''
...
```

#### <a name="apidoc.element.array-flatten.from"></a>[function <span class="apidocSignatureSpan">array-flatten.</span>from (array)](#apidoc.element.array-flatten.from)
- description and source-code
```javascript
function flattenFrom(array) {
  return flattenDown(array, [])
}
```
- example usage
```shell
...
flatten([1, [2, [3, [4, [5], 6], 7], 8], 9])
//=> [1, 2, 3, 4, 5, 6, 7, 8, 9]

flatten.depth([1, [2, [3, [4, [5], 6], 7], 8], 9], 2)
//=> [1, 2, 3, [4, [5], 6], 7, 8, 9]

(function () {
  flatten.from(arguments) //=> [1, 2, 3]
})(1, [2, 3])
'''

### Methods

* **flatten(array)** Flatten a nested array structure
* **flatten.from(arrayish)** Flatten an array-like structure (E.g. arguments)
...
```

#### <a name="apidoc.element.array-flatten.fromDepth"></a>[function <span class="apidocSignatureSpan">array-flatten.</span>fromDepth (array, depth)](#apidoc.element.array-flatten.fromDepth)
- description and source-code
```javascript
function flattenFromDepth(array, depth) {
  if (typeof depth !== 'number') {
    throw new TypeError('Expected the depth to be a number')
  }

  return flattenDownDepth(array, [], depth)
}
```
- example usage
```shell
...
'''

### Methods

* **flatten(array)** Flatten a nested array structure
* **flatten.from(arrayish)** Flatten an array-like structure (E.g. arguments)
* **flatten.depth(array, depth)** Flatten a nested array structure with a specific depth
* **flatten.fromDepth(arrayish, depth)** Flatten an array-like structure with a specific depth

## License

MIT

[npm-image]: https://img.shields.io/npm/v/array-flatten.svg?style=flat
[npm-url]: https://npmjs.org/package/array-flatten
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
