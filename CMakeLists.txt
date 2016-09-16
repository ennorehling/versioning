cmake_minimum_required(VERSION 2.8)
project(versioning C)

if(DEFINED VERSION)
set_source_files_properties(version.c PROPERTIES COMPILE_DEFINITIONS
"VERSION=\"${VERSION}\"")
endif()
add_library(version version.c)
add_executable(hello main.c)
target_link_libraries(hello version)

