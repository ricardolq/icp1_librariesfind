cmake_minimum_required(VERSION 3.10)
project(MyLibraryFindExample C)

set(mymath_DIR $ENV{HOME}/ie/cp1/install/cmake/)
message(STATUS "mymath_DIR: ${mymath_DIR}")
find_package(mymath REQUIRED)
add_executable(example src/example.c)

target_link_libraries(example PRIVATE mymath)