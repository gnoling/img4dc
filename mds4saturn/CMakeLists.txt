
set(MDS4SATURN_SOURCES
    src/console.c
    src/imgwrite.c
    src/main.c
    src/mdfwrt.c
    src/mdsaudio.c
    src/mdsdata.c
    src/tools.c
)

add_executable(mds4saturn ${MDS4SATURN_SOURCES})
target_include_directories(mds4saturn PRIVATE 
    ${CMAKE_CURRENT_SOURCE_DIR}/inc
    ${CMAKE_SOURCE_DIR}/edc/inc
)

target_link_libraries(mds4saturn edc)
