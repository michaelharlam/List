cmake_minimum_required(VERSION 3.27)
project(List LANGUAGES C)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -O2")
enable_testing()
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/bin)
set(PROJECT_SOURCES "main.c" "list.c" )
# set(TEST_SOURCES "tests.c" "list.c")

add_executable(main ${PROJECT_SOURCES})
# add_executable(testList ${TEST_SOURCES})



add_test(NAME "List Test" COMMAND testList)
