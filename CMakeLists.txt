cmake_minimum_required(VERSION 2.8.9)

project(ResectionPlanner)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://www.example.com/Slicer/Extensions/ResectionPlanner")
set(EXTENSION_CATEGORY "IGT")
set(EXTENSION_CONTRIBUTORS "Matt Lougheed (Queen's University)")
set(EXTENSION_DESCRIPTION "Modules for surgical resection planning.")
set(EXTENSION_ICONURL "http://www.example.com/Slicer/Extensions/ResectionPlanner.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/ResectionPlanner/Screenshots/1.png")

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(ResectionPath)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
