cmake_minimum_required(VERSION 3.23.0)

set(SOURCES
    main.cpp
    common.c
    args.c
)

add_executable(clonegit 
    ${SOURCES}
)

target_include_directories(clonegit 
    PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/../external/libgit2/include
)

target_link_libraries(clonegit PUBLIC git2)
