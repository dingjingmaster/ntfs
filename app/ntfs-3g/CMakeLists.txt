FILE(GLOB NTFS_3G_SRC
        ntfs-3g_common.c ntfs-3g_common.h
)

add_executable(ntfs-3g ntfs-3g.c ${NTFS_3G_SRC})
target_include_directories(ntfs-3g
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-3g PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)
target_compile_definitions(ntfs-3g PUBLIC -D_FILE_OFFSET_BITS=64)
