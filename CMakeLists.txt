# Required as the first line
cmake_minimum_required(VERSION 3.5)

# Define the crrent project
project(main VERSION 0.1)

# Tell Abseil which C++ standard to use
set(CMAKE_CXX_STANDARD 11)

# Tell CMake how to find both abseil and googletest
add_subdirectory(abseil-cpp)
add_subdirectory(googletest)

# Create a simple library
add_library(hello STATIC hello.cc hello.h)
target_link_libraries(hello absl::strings)

# Create a simple test
add_executable(hello_test hello_test.cc)
target_link_libraries(hello_test hello gtest gtest_main)

# Create a simple executable
add_executable(hello_main hello_main.cc)
target_link_libraries(hello_main hello absl::strings)

# Register the test so ctest will find it
include(CTest)
add_test(hello_test hello_test)

