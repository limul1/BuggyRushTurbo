cmake_minimum_required(VERSION 3.22.1)
project(BuggyRushTurbo LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(BUILD_GAMES OFF CACHE BOOL "" FORCE)
set(BUILD_SHARED_LIBS OFF CACHE BOOL "" FORCE)
set(CUSTOMIZE_BUILD ON CACHE BOOL "" FORCE)

include(FetchContent)
FetchContent_Declare(raylib
    GIT_REPOSITORY https://github.com/raysan5/raylib.git
    GIT_TAG 5.5
    GIT_SHALLOW TRUE)
FetchContent_MakeAvailable(raylib)

if(ANDROID)
    add_library(main SHARED src/main.cpp)
    target_link_libraries(main PRIVATE raylib android log EGL GLESv2 OpenSLES dl m)
    target_link_options(main PRIVATE "-u" "ANativeActivity_onCreate")
else()
    add_executable(BuggyRush src/main.cpp)
    target_link_libraries(BuggyRush PRIVATE raylib)
endif()
