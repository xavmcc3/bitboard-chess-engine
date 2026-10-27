cmake_minimum_required(VERSION 3.15)
project(chessengine C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_FLAGS_RELEASE "-O3 -Wall -Wextra")

add_subdirectory(src)

# Create the chessengine_uci executable
add_executable(chessengine_uci apps/uci_main.c)

# Link executable with chessengine_lib
target_link_libraries(chessengine_uci PRIVATE chessengine_lib)

# Public headers
target_include_directories(chessengine_uci PRIVATE include)

# Sandbox configuration
add_executable(sandbox apps/sandbox.c)
target_link_libraries(sandbox PRIVATE chessengine_lib)
target_include_directories(sandbox PRIVATE include)