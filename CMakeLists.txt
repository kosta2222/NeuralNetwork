cmake_minimum_required(VERSION 3.8)

project("NeuralNetwork")

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17 -pthread")

find_package(Threads REQUIRED)

file(GLOB_RECURSE HEADER_FILES "include/*.h")
file(GLOB_RECURSE SOURCE_FILES "src/*.cpp")

add_executable(${PROJECT_NAME} main.cpp ${HEADER_FILES} ${SOURCE_FILES})

#target_link_libraries(${PROJECT_NAME} PUBLIC LIBS_FOR_LINK)
target_include_directories(${PROJECT_NAME} PUBLIC include)
include_directories(include)