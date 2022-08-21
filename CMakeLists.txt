cmake_minimum_required(VERSION 3.0.0)
project(learn-opengl VERSION 0.1.0)

INCLUDE_DIRECTORIES(
    /Users/aadilsingal/vcpkg/installed/arm64-osx/include
)

LINK_DIRECTORIES(
    /Users/aadilsingal/vcpkg/installed/arm64-osx/lib
)

file(GLOB SRC CONFIGURE_DEPENDS "src/*.cpp")

add_executable(opengl-stuff ${SRC})

TARGET_LINK_LIBRARIES(opengl-stuff
    libglad.a
    libglfw3.a
)