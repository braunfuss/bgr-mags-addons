SET(TEST_TARGET magstest)

SET(TEST_SOURCES test.cpp filter.cpp)

SC_ADD_EXECUTABLE(TEST ${TEST_TARGET})
SC_LINK_LIBRARIES_INTERNAL(${TEST_TARGET} client)

SET(DETECTOR_TARGET magsdetector)
SET(DETECTOR_SOURCES main.cpp app.cpp detector.cpp filter.cpp)

SC_ADD_EXECUTABLE(DETECTOR ${DETECTOR_TARGET})
SC_LINK_LIBRARIES_INTERNAL(${DETECTOR_TARGET} client)

SC_INSTALL_INIT(${DETECTOR_TARGET} ../../../trunk/apps/templates/initd.py)

FILE(GLOB descs "${CMAKE_CURRENT_SOURCE_DIR}/descriptions/*.xml")
INSTALL(FILES ${descs} DESTINATION ${SC3_PACKAGE_APP_DESC_DIR})
