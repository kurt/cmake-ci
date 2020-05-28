# this is the beginning


cmake_minimum_required(VERSION 3.5)

project(this_one)

SET(GCC_COVERAGE_COMPILE_FLAGS "-g -O0 -coverage -fprofile-arcs -ftest-coverage")
SET(GCC_COVERAGE_LINK_FLAGS    "-coverage -lgcov")
SET( CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} ${GCC_COVERAGE_COMPILE_FLAGS}" )
SET( CMAKE_EXE_LINKER_FLAGS  "${CMAKE_EXE_LINKER_FLAGS} ${GCC_COVERAGE_LINK_FLAGS}" )

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/executables)


add_executable(HelloWorld hello_world.cpp)
add_executable(HelloWorldC hello_world.c)

#COMMAND HelloWorld
#COMMAND HelloWorldC
#COMMAND(echo "test")
#target_compile_definitions(HelloWorld PRIVATE -coverage)
#set_target_properties(HelloWorld PUBLIC test)

