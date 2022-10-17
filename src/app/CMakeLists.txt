add_executable(makesearchable makesearchable.c)
set(C_STANDARD C17)
set(C_STANDARD_REQUIRED True)
target_include_directories(makesearchable PUBLIC
$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/src/include>
)