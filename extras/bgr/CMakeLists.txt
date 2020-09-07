SC_BEGIN_PACKAGE(BGR)

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/seiscomp/src/base/common/libs)
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_BINARY_DIR}/seiscomp/src/base/common/libs)

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/../seiscomp/src/base/common/libs)
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_BINARY_DIR}/../seiscomp/src/base/common/libs)

SUBDIRS(apps)
