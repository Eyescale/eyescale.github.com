
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
"    <link rel=\"stylesheet\" href=\"stylesheet.css\" type=\"text/css\">"
"  </head>\n"
"  <body>\n"
"  <table>\n"
"    <tr><th>Project</th><th>Versions</th>"
)

file(GLOB ENTRIES RELATIVE ${CMAKE_SOURCE_DIR} *-*)
list(SORT ENTRIES)
set(PREVIOUS)
set(PREVIOUS_PROJECT)
foreach(ENTRY ${ENTRIES})
  add_custom_target(${ENTRY} ALL "${GIT_EXECUTABLE}" add ${ENTRY}
    WORKING_DIRECTORY "${CMAKE_SOURCE_DIR}"
    DEPENDS ${PREVIOUS} # serialize git invocations
    COMMENT "Adding new files in ${ENTRY}" VERBATIM)

  string(REGEX REPLACE "^(.+)-.+$" "\\1" PROJECT ${ENTRY})
  string(REGEX REPLACE "^.+-(.+)$" "\\1" VERSION ${ENTRY})
  if(NOT PROJECT STREQUAL PREVIOUS_PROJECT)
  file(APPEND index.html
    "</tr>\n"
    "    <tr><th>${PROJECT}</th>")
  endif()

  file(APPEND index.html
    "<td><a href=\"${ENTRY}/index.html\">${VERSION}</a></td>")
  set(PREVIOUS ${ENTRY})
  install(DIRECTORY ${ENTRY} DESTINATION share/eyescale)
endforeach()

file(APPEND index.html
"</tr>\n"
"  </table>\n"
"  </body>\n"
"</html>\n"
)

install(FILES index.html DESTINATION share/eyescale)
