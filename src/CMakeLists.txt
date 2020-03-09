add_definitions(-DYY_NEVER_INTERACTIVE)
include_directories(${libcuefile_SOURCE_DIR}/include)

add_library(cuefile cd cdtext cue_parse cue_print cue_scan cuefile time toc toc_parse toc_print toc_scan)
set_target_properties(cuefile PROPERTIES OUTPUT_NAME cuefile CLEAN_DIRECT_OUTPUT 1 VERSION 0.0.0 SOVERSION 0)

install(TARGETS cuefile RUNTIME LIBRARY DESTINATION "lib${LIB_SUFFIX}" ARCHIVE DESTINATION "lib${LIB_SUFFIX}")
