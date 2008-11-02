add_definitions(-DYY_NEVER_INTERACTIVE)
include_directories(${libcuefile_SOURCE_DIR}/include)
add_library(cuefile STATIC cd cdtext cue_parse cue_print cue_scan cuefile time toc toc_parse toc_print toc_scan)