---
name: GLStats
version: "0.3"
major: 0
minor: 3
description: 
updated: 14/10/15
homepage: https://github.com/Eyescale/GLStats
repository: https://github.com/Eyescale/GLStats.git
issuesurl: https://github.com/Eyescale/GLStats/issues
packageurl: https://launchpad.net/~bbp/+archive/ppa
license: 
maturity: EP
maintainers: 
contributors:  
  - Stefan Eilemann    77.6%
  - Daniel Nachbaur    15.1%
  - Daniel Pfeifer     1.7%
  - Fabien Delalondre  1.3%
  - marwan-abdellah    0.8%
  - Dardo D Kleiner    0.7%
  - Raphael Dumusc     0.6%
  - Cedric Stalder     0.5%
  - Ahmet Bilgili      0.5%
  - Juan Hernando      0.5%
  - Marwan             0.2%
  - nikolay_lukash     0.1%
  - Carsten Rohn       0.1%
  - Glendon Holst      0.1%
  - Jafet Villafranca  0.1%
  - Sarah Amsellem     0.1%
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

