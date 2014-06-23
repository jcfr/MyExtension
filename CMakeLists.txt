cmake_minimum_required(VERSION 2.8.9)

project(MyExtension)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/jcfr/MyExtension")
set(EXTENSION_CATEGORY "Examples")
set(EXTENSION_CONTRIBUTORS "Jc (Kitware)")
set(EXTENSION_DESCRIPTION "This is an example of a simple extension. Yeahh")
set(EXTENSION_ICONURL "https://raw.github.com/jcfr/MyExtension/master/MyExtension.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/MyExtension/Screenshots/1.png")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(MyCLI)
add_subdirectory(MyScripted)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
