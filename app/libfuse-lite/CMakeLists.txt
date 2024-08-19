file(GLOB FUSE_LITE_SRC
        fuse.c
        fuse_i.h
        fuse_kern_chan.c
        fuse_loop.c
        fuse_lowlevel.c
        fuse_misc.h
        fuse_opt.c
        fuse_session.c
        fuse_signals.c
        fusermount.c
        helper.c
        mount.c
        mount_util.c mount_util.h
)
add_library(libfuse-lite STATIC ${FUSE_LITE_SRC})
target_include_directories(libfuse-lite PUBLIC
        ${CMAKE_SOURCE_DIR}/app
        ${CMAKE_SOURCE_DIR}/app/include/fuse-lite
)
set_target_properties(libfuse-lite PROPERTIES OUTPUT_NAME "libfuse-lite")
