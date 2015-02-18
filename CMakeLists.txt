cmake_minimum_required(VERSION 2.8)
 
project(ICBMBrainAtlas)

configure_file(${ICBMBrainAtlas_SOURCE_DIR}/ICBMBrainAtlas.config.in  ${ICBMBrainAtlas_BINARY_DIR}/ICBMBrainAtlas.config @ONLY)

set(ATLAS_NAME ICBMBrainAtlas)
set(ATLAS_VOLUME ${ICBMBrainAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}Volume.nrrd)
set(ATLAS_VOLUME_NAME ${ATLAS_NAME}Volume)
set(ATLAS_COLOR_TABLE ${ICBMBrainAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}Colors.ctbl)
set(ATLAS_COLOR_TABLE_NAME ${ATLAS_NAME}Colors)
set(ATLAS_LABELS ${ICBMBrainAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}Labels.nrrd)
set(ATLAS_LABELS_NAME ${ATLAS_NAME}Labels)
set(MRML_FILENAME ${ICBMBrainAtlas_SOURCE_DIR}/Atlas/${ATLAS_NAME}.mrml.in)

configure_file(${ICBMBrainAtlas_SOURCE_DIR}/Atlas/ICBMBrainAtlas.mrml.in  ${ICBMBrainAtlas_BINARY_DIR}/ICBMBrainAtlas.mrml @ONLY)
