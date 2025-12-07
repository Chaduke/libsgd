## Welcome to LibSGD (Chaduke's Experimental Fork)

LibSGD is a simple game development library that provides a high level, easy to use 'scene graph' style API for writing games and apps.

LibSGD also supports loading and playing audio and will eventually include network functionality.

The library is coded in C++, but the primary public API is pure 'C', making it highly compatible with a wide range of platforms and languages.

I (Chaduke) am primarily using this version to experiment with adding LibSGD as a backend to Blitz3D in a 32-bit environment.

LibSGD is licensed under the Zlib/PNG license.

### CMake build instuctions for 32 bit Windows 10

* Install git, cmake, python3 and Visual Studio Community 2026

* Clone this repository, CD to checkout dir and:

* Configure: ``cmake -S . -B cmake-build-windows-release -G "Visual Studio 18 2026"``

* Build: ``cmake --build cmake-build-windows-release --config Release``

* Install: ``cmake --install cmake-build-windows-release --config Release``

After install, output files should end up in cmake-build-windows-release/LIBSGD_INSTALL dir.

Copy the contents of the libsgd folder from cmake-build-windows-release folder into the libsgd folder in your Blitz3D_Soloud folder.

Compile Blitz3D_Soloud

### Build instructions for html help files

* Install Doxygen.

* Set the cmake option SGD_DOXYGEN_TARGET_ENABLED to ON. You can do this by passing -DSGD_DOXYGEN_TARGET_ENABLED=ON to cmake when configuring.  

After building and installing, LIBSGD_INSTALL should include an additional html directory containing the SGD html help files.
