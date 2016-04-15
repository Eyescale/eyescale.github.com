
# Copyright (c) 2012-2016 Stefan Eilemann <eile@eyescale.ch>

cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(Eyescale VERSION 2016.04)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/CMake
  ${CMAKE_SOURCE_DIR}/CMake/common)
set(eyescale_SKIP_FIND ON PARENT_SCOPE) # for superprojects
