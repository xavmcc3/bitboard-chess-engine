# Collect library source files
set(LIB_SOURCES
    bitboard.c
)

# Define this folder's output as a static library
add_library(chessengine_lib STATIC ${LIB_SOURCES})

# Tell the library where its internal headers and public headers are
target_include_directories(chessengine_lib
    PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/../include>
    PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}
)