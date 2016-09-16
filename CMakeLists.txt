cmake_minimum_required(VERSION 2.8)
project(version C)

if(DEFINED VERSION)
#add_definitions(-DVERSION="${VERSION}")
set_source_files_properties(version.c PROPERTIES COMPILE_DEFINITIONS
"VERSION=\"${VERSION}\"")
endif()

add_executable(version version.c main.c)
