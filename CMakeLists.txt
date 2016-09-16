cmake_minimum_required(VERSION 2.8)
project(version C)

if(DEFINED VERSION)
set_source_files_properties(version.c PROPERTIES COMPILE_DEFINITIONS
"VERSION=\"${VERSION}\"")
endif()
add_library(version OBJECT version.c)
add_executable(hello main.c $<TARGET_OBJECTS:version>)

