cmake_minimum_required (VERSION 3.8)

set (CMAKE_CXX_STANDARD)

project (dvision)

include_directories (${PROJECT_SOURCE_DIR}/include/dvision)

file (GLOB "${PROJECT_NAME}_SRCS" ${PROJECT_SOURCE_DIR}/src/*.cc)

message ( ${${PROJECT_NAME}_SRCS} )

add_library (${PROJECT_NAME} STATIC SHARED ${${PROJECT_NAME}_SRCS})

add_subdirectory (example)
