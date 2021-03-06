granne\*
--------
--------

**granne** (**g**raph-based **r**etrieval of **a**pproximate **n**earest **ne**ighbors) is a Rust library for ANN-search based on Hierarchical Navigable Small World (HNSW) graphs (see https://arxiv.org/abs/1603.09320).

## Features
- Memory-mapped
- Multithreaded index creation
- Extensible indexes (add elements to an already built index)
- Python bindings
- Dense `float` or `int8` elements (cosine distance)

## Installation

#### Requirements

`granne` is dependent on `BLAS` (https://en.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms) for some computations. This applies both to the rust and python versions. On Debian/Ubuntu both `libblas-dev` and `libopenblas-dev` should work, with the latter being significantly faster.

#### Rust

```
# build
cargo build --release

# test
cargo test

# bench
cargo +nightly bench
```

#### Python

To quickly install:

```
pip install setuptools_rust
pip install .
```

To build python wheels for python 2.7, 3.4, 3.5 and 3.6 (requires docker).
```
docker build -t granne_manylinux docker/manylinux/
docker run -v $(pwd):/granne/ granne_manylinux /opt/build_wheels.sh
```
The output is written to `wheels/` and can be installed by
```
pip install granne --no-index -f wheels/
```


## Index Creation
...

## Search
...

\***granne** is Swedish and means **neighbor**