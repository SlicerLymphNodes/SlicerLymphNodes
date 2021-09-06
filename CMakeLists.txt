cmake_minimum_required(VERSION 3.13.4)

project(SlicerLymphNodes)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/SlicerLymphNodes")
set(EXTENSION_CATEGORY "Quantification")
set(EXTENSION_CONTRIBUTORS "Steve Pieper (Isomics, Inc.), Alireza Mehrtash (Brigham and Women's Hospital)")
set(EXTENSION_DESCRIPTION "Tools for segmenting and quantifying lymph nodes.	")
set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/SlicerLymphNodes.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/SlicerLymphNodes/Screenshots/1.png")
set(EXTENSION_DEPENDS "NA") # Specified as a list or "NA" if no dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(LymphNodeQuantifier)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
