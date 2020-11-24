cmake_minimum_required(VERSION 3.17)
project(cpp_start_example)

set(CMAKE_CXX_STANDARD 17)

# cpp_start
# fetching
include(FetchContent)
FetchContent_Declare(
        cpp_start
        GIT_REPOSITORY https://github.com/soerenpeters/cpp_start.git
        GIT_TAG        v0.1-alpha
)
FetchContent_Populate(cpp_start)

include(${CMAKE_BINARY_DIR}/_deps/cpp_start-src/CMake/cpp_starter.cmake)


add_subdirectory(src/adder)
