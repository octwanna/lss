##############################################################################
# LSS WSMP plugin
##############################################################################

cmake_minimum_required( VERSION 2.8 FATAL_ERROR )

project( LSS_WSMP CXX )
coolfluid_define_plugin( LSS_WSMP ${CMAKE_CURRENT_SOURCE_DIR} )

set( CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake" ${CMAKE_MODULE_PATH} )

if( CF3_PLUGIN_LSS AND CF3_PLUGIN_LSS_WSMP )
  coolfluid_find_orphan_files()
  include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )
  add_subdirectory( cf3 )
endif()
