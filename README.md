# BFM

Big F'ing Matrix.
Final assignment for LEPL1110 (Finite Element Method).

## Building

This repo is composed of two components; the backend `libbfm`, which implements all the routines BFM defines, and the frontend `pybfm`, which includes a thin Python wrapper above `libbfm` and visualisation facilities.

### libbfm

This uses CMake:

```console
mkdir -p libbfm/build
cd libbfm/build
cmake ..
make install
```

### pybfm

First, the FFI bindings to `libbfm` must be generated:

```console
python pybfm/bfm/gen_libbfm.py
```

Then, you may install the `bfm` Python module itself:

```console
pip install --user ./pybfm
```

## Running

Assuming everything is built, you can run a simple example as such:

```console
python examples/deformation.py
```
