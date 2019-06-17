# Abseil CMake Quick Start #

Make sure that [CMake is installed](https://cmake.org/install/)
on your system.

Grab this repo and initialize the subrepos for abseil and googletest.

```bash
$ git clone --branch cmake https://github.com/abseil/abseil-hello abseil-hello
...
$ cd abseil-hello
$ git submodule update --init
...
```

Configure cmake with an out of directory build.

```bash
mkdir build
cd build
cmake ..  # configure the project
```

Build and run the example main

```bash
$ make -j 8 hello_main
...
$ ./hello_main CMake
Hello CMake
```

Build and run the test

```bash
$ make -j 8 hello_test
...
$ ctest hello_test  # or just ./hello_test
Test project abseil-hello/build
    Start 1: hello_test
1/1 Test #1: hello_test .......................   Passed    0.00 sec

100% tests passed, 0 tests failed out of 1

Total Test time (real) =   0.01 sec
```

Now you are ready to live at head!

