cmake_minimum_required(VERSION 3.0.0)
project(deduplicator VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(deduplicator solution/src/main.c)

target_include_directories(deduplicator PRIVATE solution/include)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
