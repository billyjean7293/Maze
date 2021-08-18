# version of make
cmake_minimum_required(VERSION 3.19)

# my project name(name of executable)
project(COP_2001_CLion)

# complier c++ syntax version
set(CMAKE_CXX_STANDARD 14)

# what our exe file is called and
# what source files to put in it
add_executable(COP_2001_CLion main.cpp maze_defs.h)

include_directories(/usr/local/include)

find_package(SFML 2.5 COMPONENTS system window graphics network audio REQUIRED)
include_directories(${SFML_INCLUDE_DIRS})
target_link_libraries(COP_2001_CLion sfml-system sfml-window sfml-graphics sfml-audio sfml-network)
