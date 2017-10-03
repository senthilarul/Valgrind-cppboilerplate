# Valgrind Exercise - C++ Boilerplate
[![Build Status](https://travis-ci.org/senthilarul/Valgrind-cppboilerplate.svg?branch=valgrind_exercise)](https://travis-ci.org/senthilarul/Valgrind-cppboilerplate)
[![Coverage Status](https://coveralls.io/repos/github/senthilarul/Valgrind-cppboilerplate/badge.svg?branch=valgrind_exercise)](https://coveralls.io/github/senthilarul/Valgrind-cppboilerplate?branch=valgrind_exercise)
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
## Run Valgrind test
To install valgrind
```
sudo apt install valgrind
```
To install Kcachegrind
```
sudo apt install kcachegrind
```

For identifying errors, memory leaks using valgrind
```
cd <path to repository>
valgrind --tool=memcheck --leak-check=full ./build/app/shell-app 

```
Function and Memory Profiling
```
valgrind --tool=callgrind ./build/app/shell-app
valgrind --tool=massif ./build/app/shell-app
```

The above two commands produce a callgrind.out and massif.out files respectively.

To visualize callgrind.out file we use Kcachegrind.
```
kcachegrind
```
In the application that opens up, click on open menu. Select the callgrind.out file from your repository.

To visualize massif.out file in the terminal.
```
ms_print massif.out.<process id>
```


