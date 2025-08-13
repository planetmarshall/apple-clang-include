cmake_minimum_required(VERSION 3.31)
project(apple-clang-include)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED)

add_compile_options(-v)
add_executable(test main.cpp)
find_package(GTest CONFIG REQUIRED)

target_link_libraries(test PRIVATE GTest::gtest_main)

