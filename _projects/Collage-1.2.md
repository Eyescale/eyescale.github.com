---
name: Collage
version: "1.2"
major: 1
minor: 2
description: High-performance C++ library for developing object-oriented distributed applications.
updated: 14/10/15
homepage: https://github.com/Eyescale/Collage
repository: https://github.com/Eyescale/Collage.git
issuesurl: https://github.com/Eyescale/Collage/issues
packageurl: 
license: 
maturity: EP
maintainers: 
contributors:  
  - Stefan Eilemann           76.3%
  - Daniel Nachbaur           9.1%
  - Cedric Stalder            5.3%
  - Maxim Makhinya            2.5%
  - Dardo D Kleiner           1.0%
  - Daniel Pfeifer            0.8%
  - Carsten Rohn              0.7%
  - Sarah Amsellem            0.6%
  - delyas                    0.5%
  - marwan-abdellah           0.5%
  - Marwan Abdellah           0.3%
  - Lucas Peetz Dulley        0.3%
  - Philippe Robert           0.2%
  - Ahmet Bilgili             0.2%
  - Cedric                    0.2%
  - Tobias Wolf               0.2%
  - Juan Hernando             0.2%
  - Fabien Delalondre         0.1%
  - Dustin Wueest             0.1%
  - cstalder                  0.1%
  - Raphael Dumusc            0.1%
  - ahmetbilgili              0.1%
  - Rick Arkin                0.1%
  - Matthew Dawson            0.1%
  - Bruno Stefanizze          0.1%
  - unknown                   0.0%
  - John Biddiscombe          0.0%
  - Oliver Elias              0.0%
  - U-DE\daniel_nachbaur      0.0%
  - nikolay_lukash            0.0%
  - Martin Lambers            0.0%
  - Jaroslav Škarvada          0.0%
  - Thomas McGuire            0.0%
  - Marwan                    0.0%
  - Bidur Bohara              0.0%
  - Julio Delgado             0.0%
  - Theo Diefenthal           0.0%
  - Enrique G. Paredes        0.0%
  - Stefan Hutter             0.0%
  - Madhusudhanan Srinivasan  0.0%
  - bilgili                   0.0%
  - Jafet Villafranca         0.0%
  - MichaelVlad               0.0%
  - Dardo                     0.0%
readmetype: text/x-markdown
---
[TOC]

# Introduction {#Introduction}

Collage is a cross-platform C++ library for building heterogenous, distributed
applications. Among other things, it is the cluster backend for the [Equalizer
parallel rendering framework](https://github.com/Eyescale/Equalizer). Collage
provides an abstraction of different network connections, peer-to-peer
messaging, node discovery, synchronization and high-performance,
object-oriented, versioned data distribution. Collage is designed for
low-overhead multi-threaded execution which allows applications to easily
exploit multi-core architectures.

The
[API documentation](http://eyescale.github.io/Collage-1.2/index.html) can be
found on [eyescale.github.io](http://eyescale.github.io/). As with any open
source project, the available source code, in particular the
[unit tests](https://github.com/Eyescale/Collage/tree/1.2/tests) provide a
reference for developing applications.

Technical questions can be posted to the Equalizer
[Developer Mailing List](http://www.equalizergraphics.com/cgi-bin/mailman/listinfo/eq-dev),
or directly to
[info@equalizergraphics.com](mailto:info@equalizergraphics.com?subject=Collage%20question).

Commercial support, custom software development and porting services are
available from [Eyescale](http://www.eyescale.ch). Please contact
[info@eyescale.ch](mailto:info@eyescale.ch?subject=Collage%20support)
for further information.

# Features {#Features}

Collage provides different levels of abstraction to facilitate the
development distributed applications:

* Network Connections: stream-oriented point-to-point and reliable multicast
  connections for TCP/IP, SDP, InfiniBand RDMA, UDT, events, named and anonymous
  pipes, memory buffers and reliable multicast over UDP.
* Peer-to-Peer Messaging: Endian-safe node-to-node message communication with
  thread-aware message dispatch.
* Synchronization: Distributed barriers and synchronous messaging.
* Object data distribution: high-performance, object-oriented, versioned data
  distribution for C++ objects based on delta serialization.

# Building {#Building}

Collage is a cross-platform library, designed to run on any modern operating
system, including all Unix variants and the Windows operating system. Collage
uses CMake to create a platform-specific build environment. The following
platforms and build environments are tested:

* Linux: Ubuntu 14.04, RHEL 6.6 (Makefile, Ninja)
* Windows: 7 (Visual Studio 2012)
* Mac OS X: 10.8 (Makefile, Ninja)

~~~
git clone https://github.com/Eyescale/Collage.git
cd Collage
mkdir build
cd build
cmake ..
make
~~~

