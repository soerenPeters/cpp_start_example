# cpp_start example
![CI](https://github.com/soerenPeters/cpp_start_example/workflows/build/badge.svg)

This is an cpp example which make use of the cmake structure from [cpp_start](https://github.com/soerenPeters/cpp_start).

cpp_start can easily be integrated in the top level [CMakeLists.txt](CMakeLists.txt):
```cmake
include(FetchContent)
FetchContent_Declare(
        cpp_start
        GIT_REPOSITORY https://github.com/soerenpeters/cpp_start.git
        GIT_TAG        v0.1-alpha
)
FetchContent_Populate(cpp_start)

include(${CMAKE_BINARY_DIR}/_deps/cpp_start-src/CMake/cpp_starter.cmake)
```

Afterwards [targets](src/adder/CMakeLists.txt) can be created as in cpp_start:

```cmake
project(project_name CXX)

set(TARGET_NAME
        my_target_name)

set(SOURCE_FILES
        foo.cpp)

set(TEST_FILES
        test_foo.cpp)

set(PUBLIC_LINK)

add_target(BUILDTYPE static)
```