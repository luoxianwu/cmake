cmake_minimum_required(VERSION 3.10)
project(HelloWorld)

# Set C++ standard
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add executable
add_executable(HelloWorld
    src/main.cpp
    src/model1/m1.cpp
    src/model2/m2.cpp
)

# Include directories
target_include_directories(HelloWorld PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/src
    ${CMAKE_CURRENT_SOURCE_DIR}/src/model1
    ${CMAKE_CURRENT_SOURCE_DIR}/src/model2
)
