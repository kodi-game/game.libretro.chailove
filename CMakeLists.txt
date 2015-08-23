project(game.libretro.beetle-bsnes)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(beetle-bsnes REQUIRED)

set(DEPLIBS beetle-bsnes)
set(BEETLE_BSNES_CUSTOM_BINARY ${BEETLE_BSNES_LIB}
                           game.libretro.beetle-bsnes${CMAKE_SHARED_LIBRARY_SUFFIX} beetle-bsnes)

build_addon(game.libretro.beetle-bsnes BEETLE_BSNES DEPLIBS)