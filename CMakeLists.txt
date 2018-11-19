cmake_minimum_required(VERSION 3.1)
project(game.libretro.chailove)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(CHAILOVE_LIB NAMES chailove_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(CHAILOVE_CUSTOM_BINARY ${CHAILOVE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} CHAILOVE "")

include(CPack)
