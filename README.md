# cpp-boiler

## Purpose

Ever get sick of writing out the same boilerplate code for your C++ projects? Well, I do and this is why I created this repository :wink:
This repository serves as a super simple boilerplate that utilises CMake to generate compiler configuration files for your C++ project.

Right now this is pretty barebones, as projects go on the intention is to keep building upon this to hopefully more useful than just a "Hello World".

## Getting Started

### Prerequisites

- C++ compiler toolset (VC, Clang, GCC etc.)
- CMake >= 3.10

### Create your own repo with GitHub Templates

Instead of forking, you can simply create your own repo using the templates feature :grin:

### Layout

The layout is quite simple, currently there are two main subdirectories:
 - `src`: Source files, each module should live in its own subdirectory, take a look at `hello-world`.
 - `tests`: Unit tests, should shadow your source directory structure.
