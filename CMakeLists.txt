cmake_minimum_required (VERSION 3.15)

project (libkohn_avi LANGUAGES C)

include_directories(${PROJECT_SOURCE_DIR}/source)
aux_source_directory(${PROJECT_SOURCE_DIR}/source source_files)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)
set(head_files ${PROJECT_SOURCE_DIR}/source/kohn_avi.h)
add_library(libkohn_avi SHARED ${source_files})

install(FILES ${head_files} DESTINATION ${PROJECT_BINARY_DIR}/include) 
install(TARGETS libkohn_avi DESTINATION ${PROJECT_BINARY_DIR}/lib) 
