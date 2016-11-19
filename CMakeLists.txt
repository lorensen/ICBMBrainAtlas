cmake_minimum_required(VERSION 2.8)
 
get_filename_component(PROG ${CMAKE_SOURCE_DIR} NAME)
project(${PROG})

set(ATLAS_NAME ${PROJECT_NAME})
set(ATLAS_VOLUME ${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}Volume.nrrd)
set(ATLAS_VOLUME_NAME ${ATLAS_NAME}Volume)
set(ATLAS_COLOR_TABLE ${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}Colors.ctbl)
set(ATLAS_COLOR_TABLE_NAME ${ATLAS_NAME}Colors)
set(ATLAS_LABELS ${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}Labels.nrrd)
set(ATLAS_LABELS_NAME ${ATLAS_NAME}Labels)
set(MRML_FILENAME ${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in)

configure_file(${CMAKE_SOURCE_DIR}/${ATLAS_NAME}.config.in  ${CMAKE_BINARY_DIR}/${ATLAS_NAME}.config @ONLY)

configure_file(${CMAKE_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in  ${CMAKE_BINARY_DIR}/${ATLAS_NAME}.mrml @ONLY)
