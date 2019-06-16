# Abseil Bazel Quick Start #

Make sure that [Bazel is installed](https://docs.bazel.build/versions/master/install.html)
on your system.

Grab this repo

```bash
$ git clone --branch bazel https://github.com/abseil/abseil-hello abseil-hello
...
$ cd abseil-hello
```

Build and run the example

```bash
$ bazel run //:hello_main -- Bazel
...
Hello Bazel
```

Build and run the test

```bash
$ bazel test //:hello_test
...
//:hello_test                                                            PASSED in 0.1s

Executed 1 out of 1 test: 1 test passes.
```

Now you are ready to live at head!

