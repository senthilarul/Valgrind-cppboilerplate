# Valgrind Exercise - C++ Boilerplate
[![Build Status](https://travis-ci.org/dpiet/cpp-boilerplate.svg?branch=master)](https://travis-ci.org/dpiet/cpp-boilerplate)
[![Coverage Status](https://coveralls.io/repos/github/dpiet/cpp-boilerplate/badge.svg?branch=master)](https://coveralls.io/github/dpiet/cpp-boilerplate?branch=master)
---

## Overview

Exercise to identify and fix errors in C++ Boilerplate Valgrind_excercise branch.
The valgrind command is used to identify memory leaks, uninitialized variables in the program and for function and memory profiling.

Kcachegrind is used to visualize the callgrind.out file. 
ms_print is used to produce a visualization of massif.out in the terminal.

All the output file are in the "Results" directory.

The cpp-boilerplate is a simple starter C++ project with:

- cmake
- googletest

## Standard install via command-line
```
git clone --recursive https://github.com/senthilarul/Valgrind-cppboilerplate.git
cd <path to repository>
mkdir build
cd build
cmake ..
make
Run tests: ./test/cpp-test
Run program: ./app/shell-app
```

