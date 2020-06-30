cmake_minimum_required(VERSION 2.8) 

project(testApp)

add_executable(testApp main.cpp)

find_package(Boost REQUIRED COMPONENTS)
find_package(fmt REQUIRED)
find_package(restinio REQUIRED)

target_link_libraries(testApp PUBLIC http_parser)
target_link_libraries(testApp PUBLIC fmt::fmt)
target_link_libraries(testApp PUBLIC pthread)

set_property(TARGET testApp PROPERTY CXX_STANDARD 14)

