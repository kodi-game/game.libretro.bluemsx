cmake_minimum_required(VERSION 3.1)
project(game.libretro.bluemsx)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-bluemsx REQUIRED)

set(DEPLIBS bluemsx)
set(BLUEMSX_CUSTOM_BINARY ${BLUEMSX_LIB}
                          ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BLUEMSX DEPLIBS)
