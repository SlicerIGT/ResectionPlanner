cmake_minimum_required(VERSION 2.8.9)

project(ResectionPlanner)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://www.slicer.org/wiki/Documentation/Nightly/Extensions/ResectionPlanner")
set(EXTENSION_CATEGORY "IGT")
set(EXTENSION_CONTRIBUTORS "Matt Lougheed (Queen's University)")
set(EXTENSION_DESCRIPTION "Modules for surgical resection planning.")
set(EXTENSION_ICONURL "https://wiki.slicer.org/slicerWiki/images/d/d6/ResectionPlannerLogo.png")
set(EXTENSION_SCREENSHOTURLS "https://www.slicer.org/w/img_auth.php/8/82/ResectionVolume_Screenshot.png")

set(EXTENSION_DEPENDS "SlicerRT") # Specified as a space separated string, a list or 'NA' if any

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
