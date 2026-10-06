cmake_minimum_required(VERSION 3.24)
project(tacklebox_game LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Engine
add_subdirectory(external/tacklebox-engine)

add_executable(tacklebox_game
    src/main.cpp
)

target_link_libraries(tacklebox_game PRIVATE tacklebox_engine)
