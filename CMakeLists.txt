CMAKE_MINIMUM_REQUIRED(VERSION 2.4)

project(libcuefile C)

include(GNUInstallDirs)

set(CMAKE_VERBOSE_MAKEFILE false)

add_subdirectory(src)
install(DIRECTORY include/ DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})
