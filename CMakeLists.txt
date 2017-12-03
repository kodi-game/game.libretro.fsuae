cmake_minimum_required(VERSION 3.1)
project(game.libretro.fsuae)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-fsuae REQUIRED)

set(FSUAE_CUSTOM_BINARY ${FSUAE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} FSUAE "")
