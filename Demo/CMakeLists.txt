cmake_minimum_required(VERSION 3.30)
project(Demo)
set(CMAKE_CXX_STANDARD 17)

set(SFML_DIR "D:/sfml/SFML-3.0.0/lib/cmake/SFML")

find_package(SFML 3 REQUIRED COMPONENTS Graphics System Window Audio Network)

add_executable(Demo main.cpp)

target_link_libraries(Demo PRIVATE
        SFML::Graphics
        SFML::System
        SFML::Window
        SFML::Audio
        SFML::Network
)