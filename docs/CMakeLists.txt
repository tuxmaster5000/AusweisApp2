IF(SPHINX_FOUND)
	SPHINX_GEN("${CMAKE_CURRENT_SOURCE_DIR}/releasenotes" "notes" BUILDER singlehtml html latex)

	SPHINX_GEN("${CMAKE_CURRENT_SOURCE_DIR}/sdk" "sdk" BUILDER changes html latex DEFAULT_LANG en)

	SPHINX_GEN("${CMAKE_CURRENT_SOURCE_DIR}/installation" "inst" BUILDER changes html latex)
ELSE()
	MESSAGE(STATUS "No documentation will be generated")
ENDIF()
