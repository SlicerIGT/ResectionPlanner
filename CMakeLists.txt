cmake_minimum_required(VERSION 2.8.9)

project(ResectionPlanner)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://www.slicer.org/slicerWiki/index.php?title=Documentation/Nightly/Extensions/ResectionPlanner")
set(EXTENSION_CATEGORY "IGT")
set(EXTENSION_CONTRIBUTORS "Matt Lougheed (Queen's University)")
set(EXTENSION_DESCRIPTION "Modules for surgical resection planning.")
set(EXTENSION_ICONURL "http://wiki.slicer.org/slicerWiki/images/d/d6/ResectionPlannerLogo.png")
set(EXTENSION_SCREENSHOTURLS "http://www.slicer.org/slicerWiki/index.php/File:ResectionVolume_Screenshot.png")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(ResectionVolume)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
