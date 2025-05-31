cmake_minimum_required(VERSION 3.24)
project(Snake)
set(CMAKE_CXX_STANDARD 17)




set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17")

set(SOURCE_FILES main.cpp Board.cpp Board.h Board.cpp Board.h View.cpp View.h Controller.cpp Controller.h)
add_executable(Snake ${SOURCE_FILES})
include_directories(/usr/local/include)

find_package(SFML 2.5 COMPONENTS system window graphics network audio REQUIRED)
include_directories(${SFML_INCLUDE_DIRS})
target_link_libraries(Snake sfml-system sfml-window sfml-graphics sfml-audio sfml-network)