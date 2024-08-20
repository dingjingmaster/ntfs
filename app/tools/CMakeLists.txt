include(../libntfs-3g/libntfs-3g.cmake)
include(../libfuse-lite/libfuse-lite.cmake)


add_executable(ntfs-fix ntfsfix.c utils.h utils.c)
target_include_directories(ntfs-fix
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-fix PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-info ntfsinfo.c utils.c utils.h)
target_include_directories(ntfs-info
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-info PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-cluster ntfscluster.c ntfscluster.h cluster.c cluster.h utils.h utils.c)
target_include_directories(ntfs-cluster
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-cluster PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-ls ntfsls.c utils.c utils.h list.h)
target_include_directories(ntfs-ls
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-ls PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-cat ntfscat.c ntfscat.h utils.h utils.c)
target_include_directories(ntfs-cat
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-cat PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-cmp ntfscmp.c utils.c utils.h)
target_include_directories(ntfs-cmp
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-cmp PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-cp ntfscp.c utils.c utils.h)
target_include_directories(ntfs-cp
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-cp PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-label ntfslabel.c utils.h utils.c)
target_include_directories(ntfs-label
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-label PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-undelete ntfsundelete.c ntfsundelete.h utils.h utils.c list.h)
target_include_directories(ntfs-undelete
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-undelete PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-resize ntfsresize.c utils.c utils.h)
target_include_directories(ntfs-resize
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-resize PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-clone ntfsclone.c utils.c utils.h)
target_include_directories(ntfs-clone
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-clone PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-swipe ntfswipe.c ntfswipe.h utils.h utils.c)
target_include_directories(ntfs-swipe
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-swipe PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-truncate attrdef.h attrdef.c ntfstruncate.c utils.c utils.h)
target_include_directories(ntfs-truncate
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-truncate PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-recover playlog.c ntfsrecover.c ntfsrecover.h utils.h utils.c)
target_include_directories(ntfs-recover
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-recover PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-usermap ntfsusermap.c utils.c utils.h)
target_include_directories(ntfs-usermap
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-usermap PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-secaudit ntfssecaudit.c utils.h utils.c)
target_include_directories(ntfs-secaudit
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-secaudit PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-dump-logfile ntfsdump_logfile.c)
target_include_directories(ntfs-dump-logfile
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-dump-logfile PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-mftalloc ntfsmftalloc.c utils.c utils.h)
target_include_directories(ntfs-mftalloc
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-mftalloc PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-move ntfsmove.c ntfsmove.h utils.c utils.h)
target_include_directories(ntfs-move
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-move PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-fallocate ntfsfallocate.c utils.h utils.c)
target_include_directories(ntfs-fallocate
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfs-fallocate PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(ntfs-decrypt ntfsdecrypt.c utils.h utils.c)
target_include_directories(ntfs-decrypt
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
        ${CRYPT_INCLUDE_DIRS} ${GNU_INCLUDE_DIRS}
)
target_link_libraries(ntfs-decrypt PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        ${CRYPT_LIBRARIES} ${GNU_LIBRARIES}
        libntfs-3g libfuse-lite)

add_executable(ntfsck ntfsck.c utils.h utils.c)
target_include_directories(ntfsck
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
)
target_link_libraries(ntfsck PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite)

add_executable(mkntfs attrdef.c attrdef.h boot.c boot.h sd.c sd.h mkntfs.c utils.c utils.h ${LIB_NTFS_3G} ${FUSE_LITE_SRC})
target_include_directories(mkntfs
        PUBLIC ${CMAKE_SOURCE_DIR}/app/
        PUBLIC ${CMAKE_SOURCE_DIR}/app/include/ntfs-3g
        ${UUID_INCLUDE_DIRS}
)
target_link_libraries(mkntfs PUBLIC
        -L${CMAKE_BINARY_DIR}/app/libntfs-3g
        -L${CMAKE_BINARY_DIR}/app/libfuse-lite
        libntfs-3g libfuse-lite ${UUID_LIBRARIES})
