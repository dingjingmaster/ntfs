include(libntfs-3g.cmake)

add_library(libntfs-3g STATIC ${LIB_NTFS_3G})
target_include_directories(libntfs-3g PUBLIC
        ${CMAKE_SOURCE_DIR}/app
        ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
set_target_properties(libntfs-3g PROPERTIES OUTPUT_NAME "libntfs-3g")
