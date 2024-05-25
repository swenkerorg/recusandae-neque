# @swenkerorg/recusandae-neque <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Get the ArrayBuffer out of a TypedArray, robustly.

This will work in node <= 0.10 and < 0.11.4, where there's no prototype accessor, only a nonconfigurable own property.
It will also work in modern engines where `TypedArray.prototype.buffer` has been deleted after this module has loaded.

## Example

```js
const typedArrayBuffer = require('@swenkerorg/recusandae-neque');
const assert = require('assert');

const arr = new Uint8Array(0);
assert.equal(arr.buffer, typedArrayBuffer(arr));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@swenkerorg/recusandae-neque
[npm-version-svg]: https://versionbadg.es/inspect-js/@swenkerorg/recusandae-neque.svg
[deps-svg]: https://david-dm.org/inspect-js/@swenkerorg/recusandae-neque.svg
[deps-url]: https://david-dm.org/inspect-js/@swenkerorg/recusandae-neque
[dev-deps-svg]: https://david-dm.org/inspect-js/@swenkerorg/recusandae-neque/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@swenkerorg/recusandae-neque#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@swenkerorg/recusandae-neque.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@swenkerorg/recusandae-neque.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@swenkerorg/recusandae-neque.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@swenkerorg/recusandae-neque
[codecov-image]: https://codecov.io/gh/inspect-js/@swenkerorg/recusandae-neque/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@swenkerorg/recusandae-neque/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@swenkerorg/recusandae-neque
[actions-url]: https://github.com/inspect-js/@swenkerorg/recusandae-neque/actions
