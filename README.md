<!--

@license Apache-2.0

Copyright (c) 2020 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Node-API ndarray dtype

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> C API for returning the ndarray [data type][@stdlib/ndarray/dtypes] corresponding to a Node-API typed array type.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/ndarray-base-napi-typedarray-type-to-dtype
```

</section>

<section class="usage">

## Usage

```c
#include "stdlib/ndarray/base/napi/typedarray_type_to_dtype.h"
```

#### stdlib_ndarray_napi_typedarray_type_to_dtype( napi_typedarray_type vtype )

Returns the ndarray [data type][@stdlib/ndarray/dtypes] corresponding to a Node-API typed array type.

```c
#include "stdlib/ndarray/base/napi/typedarray_type_to_dtype.h"
#include "stdlib/ndarray/dtypes.h"
#include <node_api.h>
#include <assert.h>

// Add-on function export...
napi_value addon( napi_env env, napi_callback_info info ) {

    // ...

    // Get function arguments...
    size_t argc = 1;
    napi_value argv[ 1 ];
    napi_status status = napi_get_cb_info( env, info, &argc, argv, NULL, NULL );
    assert( status == napi_ok );

    // ...

    // Get a typed array argument...
    napi_typedarray_type vtype;
    size_t xlen;
    void *X;
    status = napi_get_typedarray_info( env, argv[ 0 ], &vtype, &xlen, &X, NULL, NULL );
    assert( status == napi_ok );

    // ...

    // Return the corresponding ndarray data type for the input typed array:
    enum STDLIB_NDARRAY_DTYPE dtype = stdlib_ndarray_napi_typedarray_type_to_dtype( vtype );

    // ...
}
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

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

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/ndarray-base-napi-typedarray-type-to-dtype.svg
[npm-url]: https://npmjs.org/package/@stdlib/ndarray-base-napi-typedarray-type-to-dtype

[test-image]: https://github.com/stdlib-js/ndarray-base-napi-typedarray-type-to-dtype/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/ndarray-base-napi-typedarray-type-to-dtype/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/ndarray-base-napi-typedarray-type-to-dtype/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/ndarray-base-napi-typedarray-type-to-dtype?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/ndarray-base-napi-typedarray-type-to-dtype.svg
[dependencies-url]: https://david-dm.org/stdlib-js/ndarray-base-napi-typedarray-type-to-dtype/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/ndarray-base-napi-typedarray-type-to-dtype/main/LICENSE

[@stdlib/ndarray/dtypes]: https://github.com/stdlib-js/ndarray-dtypes

</section>

<!-- /.links -->
