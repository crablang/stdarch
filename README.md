stdsimd - Rust's standard library SIMD components
=======

[![Travis-CI Status]][travis] [![Appveyor Status]][appveyor] [![Latest Version]][crates.io] [![docs]][docs.rs]

# Usage

`stdsimd` is now shipped with Rust's `std` library - its is part of `libcore`
and `libstd`.

The easiest way to use it is just to import it via `use std::arch`. 

The `std::arch` component for `x86` is available in stable Rust. The `std::arch`
components for other architectures requires nightly Rust. The `std::simd`
component now lives in the
[`packed_simd`](https://github.com/rust-lang-nursery/packed_simd) crate.

Using `stdsimd` master branch is not recommended. It requires nightly Rust, it
only works with particular Rust nightly versions, and it can (and does) break
often. If you need to use `stdsimd` master branch, you can add it to your
`Cargo.toml` as follows:

```toml
#[dependencies]
core_arch = { git = "https://github.com/rust-lang-nursery/stdsimd.git" }
std_detect = { git = "https://github.com/rust-lang-nursery/stdsimd.git" }
```

# Documentation

* [Documentation - i686][i686]
* [Documentation - x86\_64][x86_64]
* [Documentation - arm][arm]
* [Documentation - aarch64][aarch64]
* [Documentation - powerpc][powerpc]
* [Documentation - powerpc64][powerpc64]
* [How to get started][contrib]
* [How to help implement intrinsics][help-implement]

[contrib]: https://github.com/rust-lang-nursery/stdsimd/blob/master/CONTRIBUTING.md
[help-implement]: https://github.com/rust-lang-nursery/stdsimd/issues/40
[i686]: https://rust-lang-nursery.github.io/stdsimd/i686/stdsimd/
[x86_64]: https://rust-lang-nursery.github.io/stdsimd/x86_64/stdsimd/
[arm]: https://rust-lang-nursery.github.io/stdsimd/arm/stdsimd/
[aarch64]: https://rust-lang-nursery.github.io/stdsimd/aarch64/stdsimd/
[powerpc]: https://rust-lang-nursery.github.io/stdsimd/powerpc/stdsimd/
[powerpc64]: https://rust-lang-nursery.github.io/stdsimd/powerpc64/stdsimd/

### Approach

The main goal is to expose APIs defined by *vendors* with the least amount of
abstraction possible. On x86, for example, the API should correspond to that
provided by `emmintrin.h`.

# License

`stdsimd` is primarily distributed under the terms of both the MIT license and
the Apache License (Version 2.0), with portions covered by various BSD-like
licenses.

See LICENSE-APACHE, and LICENSE-MIT for details.


[travis]: https://travis-ci.org/rust-lang-nursery/stdsimd
[Travis-CI Status]: https://travis-ci.org/rust-lang-nursery/stdsimd.svg?branch=master
[appveyor]: https://ci.appveyor.com/project/rust-lang-libs/stdsimd/branch/master
[Appveyor Status]: https://ci.appveyor.com/api/projects/status/ix74qhmilpibn00x/branch/master?svg=true
[Latest Version]: https://img.shields.io/crates/v/stdsimd.svg
[crates.io]: https://crates.io/crates/stdsimd
[docs]: https://docs.rs/stdsimd/badge.svg
[docs.rs]: https://docs.rs/stdsimd/
