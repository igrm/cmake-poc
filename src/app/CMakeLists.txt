add_executable(makesearchable makesearchable.c)
target_include_directories(makesearchable PUBLIC "${CMAKE_SOURCE_DIR}/src/include")
target_link_libraries(makesearchable PUBLIC libsearchableutils)