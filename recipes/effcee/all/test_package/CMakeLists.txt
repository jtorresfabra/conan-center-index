cmake_minimum_required(VERSION 3.1)
project(test_package)


include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

find_package(effcee REQUIRED)

add_executable(effcee-example main.cc)

target_link_libraries(effcee-example effcee::effcee)
set_property(TARGET effcee-example PROPERTY CXX_STANDARD 11)
