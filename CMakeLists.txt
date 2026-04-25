cmake_minimum_required(VERSION 3.10)
project(Pointer)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add executable
add_executable(code test.cpp)

# Set compiler flags
if(MSVC)
    target_compile_options(code PRIVATE /W4)
else()
    target_compile_options(code PRIVATE -Wall -Wextra -Wpedantic)
endif()

# Include directory for header files
target_include_directories(code PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})