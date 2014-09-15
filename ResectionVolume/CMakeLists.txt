#-----------------------------------------------------------------------------
set(MODULE_NAME ResectionVolume)

#-----------------------------------------------------------------------------
set(MODULE_PYTHON_SCRIPTS
  ${MODULE_NAME}.py
  )

set(MODULE_PYTHON_RESOURCES
  Resources/Icons/${MODULE_NAME}.png
  )

set(TEST_RESOURCES
  TestData/RecoloredResectionVolumeTestLabel.nrrd
  TestData/ResectionVolumeModel.vtk
  TestData/ResectionVolumePoints.fcsv
  TestData/ResectionVolumeTestLabel.nrrd
  )

if (BUILD_TESTING)
  set(MODULE_PYTHON_RESOURCES
    ${MODULE_PYTHON_RESOURCES}
    ${TEST_RESOURCES}
    )
endif()

#-----------------------------------------------------------------------------
slicerMacroBuildScriptedModule(
  NAME ${MODULE_NAME}
  SCRIPTS ${MODULE_PYTHON_SCRIPTS}
  RESOURCES ${MODULE_PYTHON_RESOURCES}
  # --Currently Failing w/ non-scripted dependencies-- WITH_GENERIC_TESTS
  )

#-----------------------------------------------------------------------------
if(BUILD_TESTING)

  # Register the unittest subclass in the main script as a ctest.
  # Note that the test will also be available at runtime.
  slicer_add_python_unittest(SCRIPT ${MODULE_NAME}.py)

  # Additional build-time testing
  add_subdirectory(Testing)
endif()
