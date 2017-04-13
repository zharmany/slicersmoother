cmake_minimum_required(VERSION 2.8.9)

project(SlicerSmoother)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/SlicerSmoother")
set(EXTENSION_CATEGORY "zth")
set(EXTENSION_CONTRIBUTORS "Zachary Harmany (UC Davis)")
set(EXTENSION_DESCRIPTION "An extension for smoothing volumetric data.")
set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/SlicerSmoother.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/SlicerSmoother/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a space separated string, a list or 'NA' if any

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(GaussianSmoothing)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
