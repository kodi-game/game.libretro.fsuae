cmake_minimum_required(VERSION 3.5)
project(game.libretro.fsuae)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(FSUAE_LIB NAMES fsuae_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(FSUAE_CUSTOM_BINARY ${FSUAE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} FSUAE "")
