cmake_minimum_required(VERSION 3.28)

#SET (CMAKE_CXX_COMPILER "/usr/bin/clang++" CACHE STRING "C++ compiler" FORCE)
project(cpplearn001 LANGUAGES CXX)

add_executable(cpplearn001 main.cpp)

target_sources(cpplearn001
    PUBLIC
        FILE_SET CXX_MODULES
        FILES
            foo.ixx
            foo_part.ixx
    PRIVATE
        foo.cpp
        foo_part.cpp
)

target_compile_features(cpplearn001 PUBLIC cxx_std_20)

