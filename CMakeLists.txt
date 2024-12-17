cmake_minimum_required(VERSION 3.13)
project(SimpleLibrary VERSION 1.0 LANGUAGES CXX)

# Create Library
add_library(SimpleLibrary
    src/Greeter.cpp
)

# Add headers to library
target_include_directories(SimpleLibrary PUBLIC include)
