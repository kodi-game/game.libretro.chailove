cmake_minimum_required(VERSION 3.1)
project(game.libretro.chailove)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-chailove REQUIRED)

set(chailove_CUSTOM_BINARY ${chailove_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} chailove "")
