# cpp-boiler

## Purpose

Ever get sick of writing out the same boilerplate code for your C++ projects? Well, I do and this is why I created this repository :wink:
This repository serves as a super simple boilerplate that utilises CMake to generate compiler configuration files for your C++ project.

Right now this is pretty barebones, as projects go on the intention is to keep building upon this to hopefully more useful than just a "Hello World".

## Getting Started

### Prerequisites

- C++ compiler toolset (VC, Clang, GCC etc.)
- CMake >= 3.14
- [Conan package manager](https://docs.conan.io/en/latest/installation.html)
  - Python >= 3.5

### Create your own repo with GitHub Templates

Instead of forking, you can simply create your own repo using the templates feature :grin:

### Layout

The layout is quite simple, currently there are two main subdirectories:
 - `src`: Source files, each module should live in its own subdirectory, take a look at `hello-world`.
 - `tests`: Unit tests, one test file per module, or however many you like.

### Building & Testing

1. Fetch dependencies via Conan. Dependencies are defined in `conanfile.txt`.
```shell
mkdir build && cd build && conan install .. && cd ..
```

2. Generate compiler configuration files
```shell
cmake -S . -B build
```

3. Build
```shell
cmake --build build
```

4. Run tests ([GoogleTest](https://google.github.io/googletest/) is setup and ready to go)
```shell
cd build && ctest
```

## todos

- [ ] Setup a better file structure for the build output via CMake
- [ ] Build script, platform independent, Python?
