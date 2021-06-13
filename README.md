<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Native Function

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> [Regular expression][regexp] to match a native function.

<section class="installation">

## Installation

```bash
npm install @stdlib/regexp-native-function
```

</section>

<section class="usage">

## Usage

```javascript
var reNativeFunction = require( '@stdlib/regexp-native-function' );
```

#### reNativeFunction()

Returns a [regular expression][regexp] to match a native `function`.

```javascript
var RE_NATIVE_FUNCTION = reNativeFunction();
var bool = RE_NATIVE_FUNCTION.test( Date.toString() );
// returns true
```

#### reNativeFunction.REGEXP

[Regular expression][regexp] to match a native `function`.

```javascript
var bool = reNativeFunction.REGEXP.test( Date.toString() );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint-disable no-restricted-syntax, no-empty-function, stdlib/no-builtin-math -->

<!-- eslint no-undef: "error" -->

```javascript
var Int8Array = require( '@stdlib/array-int8' );
var reNativeFunction = require( '@stdlib/regexp-native-function' );

var RE_NATIVE_FUNCTION = reNativeFunction();
function isNativeFunction( fcn ) {
    return RE_NATIVE_FUNCTION.test( fcn.toString() );
}

var bool = isNativeFunction( Math.sqrt );
// returns true

bool = isNativeFunction( String );
// returns true

bool = isNativeFunction( Int8Array );
// returns true

bool = isNativeFunction( Date );
// returns true

bool = isNativeFunction( function noop() {} );
// returns false
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-native-function.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-native-function

[test-image]: https://github.com/stdlib-js/regexp-native-function/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/regexp-native-function/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-native-function/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-native-function?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-native-function
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-native-function/main

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-native-function/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

</section>

<!-- /.links -->
