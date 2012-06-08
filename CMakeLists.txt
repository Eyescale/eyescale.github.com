
# Copyright (c) 2012 Stefan Eilemann <eile@eyescale.ch>

cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(Documentation)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/CMake)
find_package(Git REQUIRED)

file(WRITE index.html
"<!DOCTYPE HTML PUBLIC \"-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd\">\n"
"<html>\n"
"  <head>\n"
"    <title>Eyescale API Documentation</title>\n"
"  </head>\n"
"  <body>\n"
"  <ul>\n"
)

file(GLOB ENTRIES RELATIVE ${CMAKE_SOURCE_DIR} *-*)
set(PREVIOUS)
foreach(ENTRY ${ENTRIES})
  add_custom_target(${ENTRY} ALL "${GIT_EXECUTABLE}" add ${ENTRY}
    WORKING_DIRECTORY "${CMAKE_SOURCE_DIR}"
    DEPENDS ${PREVIOUS} # serialize git invocations
    COMMENT "Adding new files in ${ENTRY}" VERBATIM)
  file(APPEND index.html
    "    <li><a href=\"${ENTRY}/index.html\">${ENTRY}</a></li>\n"
    )
  set(PREVIOUS ${ENTRY})
endforeach()

file(APPEND index.html
"  </ul>\n"
"  </body>\n"
"</html>\n"
)
