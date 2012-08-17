
# Copyright (c) 2012 Stefan Eilemann <eile@eyescale.ch>

cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(EyescalePorts)
find_package(Git REQUIRED)
add_custom_target(gitadd ALL
  COMMAND "${GIT_EXECUTABLE}" add ports
  WORKING_DIRECTORY "${CMAKE_SOURCE_DIR}"
  COMMENT "Adding new files in ports" VERBATIM)
install(DIRECTORY ports DESTINATION .)