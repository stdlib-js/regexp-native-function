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

# reNativeFunction

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Regular expression][regexp] to match a native function.



<section class="usage">

## Usage

To use in Observable,

```javascript
reNativeFunction = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-native-function@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var reNativeFunction = require( 'path/to/vendor/umd/regexp-native-function/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/regexp-native-function@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.reNativeFunction;
})();
</script>
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

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/array-int8@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/regexp-native-function@umd/browser.js"></script>
<script type="text/javascript">
(function () {

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

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/regexp/function-name`][@stdlib/regexp/function-name]</span><span class="delimiter">: </span><span class="description">return a regular expression to capture a function name.</span>
-   <span class="package-name">[`@stdlib/utils/function-name`][@stdlib/utils/function-name]</span><span class="delimiter">: </span><span class="description">determine a function's name.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-native-function.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-native-function

[test-image]: https://github.com/stdlib-js/regexp-native-function/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/regexp-native-function/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-native-function/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-native-function?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-native-function.svg
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-native-function/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/regexp-native-function/tree/deno
[umd-url]: https://github.com/stdlib-js/regexp-native-function/tree/umd
[esm-url]: https://github.com/stdlib-js/regexp-native-function/tree/esm
[branches-url]: https://github.com/stdlib-js/regexp-native-function/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-native-function/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

<!-- <related-links> -->

[@stdlib/regexp/function-name]: https://github.com/stdlib-js/regexp-function-name/tree/umd

[@stdlib/utils/function-name]: https://github.com/stdlib-js/utils-function-name/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
