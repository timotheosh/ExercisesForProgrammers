cmake_minimum_required(VERSION 2.8)
project(sol01)
link_directories("/usr/lib")
set(main_sources ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp
                 ${CMAKE_CURRENT_SOURCE_DIR}/src/Sol01.cpp)
set(gcc_cflags "-g3 -std=c++11")
set(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} ${gcc_cflags}")
set(CMAKE_EXE_LINKER_FLAGS  "${CMAKE_EXE_LINKER_FLAGS} ${gcc_cflags}")
add_executable(sol01 ${main_sources})
target_link_libraries(sol01 readline boost_program_options)
install(TARGETS sol01 RUNTIME DESTINATION bin)
