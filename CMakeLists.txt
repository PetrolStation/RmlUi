cmake_minimum_required(VERSION 3.16)

PA_NEW(RmlUi)

PA_LINK_LIBRARIES( PRIVATE RmlUi::RmlUi )

PA_INCLUDE_DIRECTORIES(
    ${CMAKE_CURRENT_SOURCE_DIR}/src
    ${CMAKE_CURRENT_SOURCE_DIR}/deps/RmlUi/Include
)

File(GLOB_RECURSE SOURCE_FILES src/*.cpp )
File(GLOB_RECURSE HEADER_FILES src/*.h   )

pa_add_source_files(
    ${SOURCE_FILES}
    ${HEADER_FILES}
)

add_subdirectory(deps)
