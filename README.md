# safe-compare
Constant-time comparison algorithm to prevent Node.js timing attacks.

For more information about Node.js timing attacks, please visit https://snyk.io/blog/node-js-timing-attack-ccc-ctf/.

[![npm package](https://img.shields.io/npm/v/safe-compare.svg?style=flat-square)](https://www.npmjs.org/package/safe-compare)
[![tag:?](https://img.shields.io/github/tag/Bruce17/safe-compare.svg?style=flat-square)](https://github.com/Bruce17/safe-compare/releases)
[![Dependency Status](https://david-dm.org/Bruce17/safe-compare.svg?style=flat-square)](https://david-dm.org/Bruce17/safe-compare)
[![devDependency Status](https://david-dm.org/Bruce17/safe-compare/dev-status.svg?style=flat-square)](https://david-dm.org/Bruce17/safe-compare#info=devDependencies)
[![Coverage Status](https://coveralls.io/repos/github/Bruce17/safe-compare/badge.svg?branch=master)](https://coveralls.io/github/Bruce17/safe-compare?branch=master)
[![Code Climate](https://codeclimate.com/github/Bruce17/safe-compare/badges/gpa.svg)](https://codeclimate.com/github/Bruce17/safe-compare)
[![Known Vulnerabilities](https://snyk.io/test/github/bruce17/safe-compare/badge.svg)](https://snyk.io/test/github/bruce17/safe-compare)
[![bitHound Overall Score](https://www.bithound.io/github/Bruce17/safe-compare/badges/score.svg)](https://www.bithound.io/github/Bruce17/safe-compare)
[![Build Status - Tarvis](https://travis-ci.org/Bruce17/safe-compare.svg?style=flat-square&branch=master)](https://travis-ci.org/Bruce17/safe-compare)
[![Build status - AppVeyor](https://ci.appveyor.com/api/projects/status/ounmeq5c4ajuu7g3/branch/master?svg=true)](https://ci.appveyor.com/project/Bruce17/safe-compare/branch/master)

## Installation

```
$ npm install safe-compare --save
```


## Usage

```javascript
var safeCompare = require('safe-compare');

safeCompare('hello world', 'hello world'); // -> true

safeCompare('hello', 'not hello'); // -> false
safeCompare('hello foo', 'hello bar'); // -> false
```


## Tests

```
$ npm test
```


## What's the improvement of this package?

This Node.js module is a improvement of the two existing modules [scmp](https://github.com/freewil/scmp) and [secure-compare](https://github.com/vdemedes/secure-compare). It uses the best parts of both implementations.

The implementation of [scmp](https://github.com/freewil/scmp) is a good base, but it has a shorter execution time if the string's length is not equal. The package [secure-compare](https://github.com/vdemedes/secure-compare) always compares the two input strings, but its implementation is not as clean as in [scmp](https://github.com/freewil/scmp).


## License

safe-compare is released under the MIT license.
