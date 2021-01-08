cmake_minimum_required(VERSION 2.8)
project(window_test)


#set(CMAKE_CXX_FLAGS "-std=c++14 -g")
#set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR})

include_directories(imgs)

find_package(wxWidgets REQUIRED COMPONENTS net core base)

include(
    ${wxWidgets_USE_FILE}
    )

FILE(GLOB_RECURSE sourcefiles "src/main.cpp")

add_executable(window.exe ${sourcefiles})
target_link_libraries(window.exe ${wxWidgets_LIBRARIES})
