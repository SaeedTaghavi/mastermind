cmake_minimum_required(VERSION 3.7)
if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release CACHE STRING "Debug or Release")
endif()
project(mastermind
LANGUAGES Fortran
VERSION 1.4.0)
enable_testing()

include(cmake/compilers.cmake)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})

add_subdirectory(src)

install(TARGETS mastermind
        RUNTIME DESTINATION bin)
