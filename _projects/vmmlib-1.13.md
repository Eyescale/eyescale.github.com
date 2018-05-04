---
name: vmmlib
version: "1.13"
major: 1
minor: 13
description: Templatized C++ vector and matrix math library
updated: 05/05/18
homepage: https://github.com/Eyescale/vmmlib
repository: https://github.com/Eyescale/vmmlib.git
issuesurl: https://github.com/Eyescale/vmmlib/issues
packageurl: https://launchpad.net/~eilemann/+archive/equalizer-dev
license: BSD
maturity: EP
maintainers: Stefan Eilemann (eile@eyescale.ch)
contributors: Cyrille Pierre Henri Favreau
readmetype: text/x-markdown
---
[TOC]

# Introduction

A templatized C++ vector and matrix math library.

VMMLib includes a vector and a matrix class, with additional
functionality for the often-used 3d and 4d vectors and 3x3 and 4x4
matrices. More advanced features include solvers, frustum computations
and frustum culling classes and spatial data structures.

VMMLib is implemented using C++ templates, making it versatile. Being a
header-only library, it is very easy to integrate into your libraries
and programs. There is no need to build and install a library, just
include the headers and you are set. The BSD license allows the usage
both in open source and commercial closed source software.

# Features

VMMLib provides the following major classes:
* Basic matrix math: vmml::vector, vmml::quaternion, vmml::matrix
* OpenGL math: vmml::Frustum, vmml::FrustumCuller, vmml::AABB
* Detailed @ref Changelog

# Bugs

Please file a [Bug Report](https://github.com/Eyescale/vmmlib/issues) if
you find any issue with this software.

# Building

VMMLib is a cross-platform library, designed to run on any modern
operating system, including all Unix variants and the Windows operating
system. It requires a C++11 compiler. VMMLib uses CMake to create a
platform-specific build environment. The following platforms and build
environments are tested:

* Linux: Ubuntu 16.04, RHEL 6.8 (Makefile, Ninja)
* Windows: 7 (Visual Studio 2012)
* Mac OS X: 10.9 (Makefile, Ninja)

Building from source is as simple as:

    git clone --recursive https://github.com/Eyescale/vmmlib.git
    mkdir vmmlib/build
    cd vmmlib/build
    cmake -GNinja ..
    ninja

