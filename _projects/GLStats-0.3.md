---
name: GLStats
version: "0.3"
major: 0
minor: 3
description: 
updated: 29/03/16
homepage: https://github.com/Eyescale/GLStats
repository: https://github.com/Eyescale/GLStats.git
issuesurl: https://github.com/Eyescale/GLStats/issues
packageurl: https://launchpad.net/~bbp/+archive/ppa
license: 
maturity: EP
maintainers: 
contributors: Ahmet Bilgili; Carsten Rohn; Cedric Stalder; Daniel Nachbaur; Daniel Pfeifer; Dardo D Kleiner; Fabien Delalondre; Glendon Holst; Jafet Villafranca; Juan Hernando; Marwan; Raphael Dumusc; Sarah Amsellem; Stefan Eilemann; marwan-abdellah; nikolay_lukash
readmetype: text/x-markdown
---
# GLStats {#glstats}

[TOC]

# About {#About}

GLStats is a generic OpenGL overlay statistics renderer used by the
Equalizer parallel rendering framework.

# Building from Source {#Build}

GLStats is a cross-platform library, designed to run on any modern
operating system, including all Unix variants and the Windows operating
system.  Zeroconf support in Lunchbox is required for the DNS_SD module
and applications. The following platforms and build environments are
tested:

* Linux: Ubuntu 14.04, RHEL 6.5 (Makefile, i386, x64)
* Windows: 7 (Visual Studio 2008, i386, x64)
* Mac OS X: 10.8 (Makefile, i386, x64)

The build system is using CMake, with the standard CMake build process:

    git clone https://github.com/Eyescale/GLStats.git
    cd GLStats
    mkdir build
    cd build
    cmake ..
    make

# Changes

* Nothing to see here, move on

