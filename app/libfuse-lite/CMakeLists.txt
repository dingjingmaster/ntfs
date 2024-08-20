include(libfuse-lite.cmake)

add_library(libfuse-lite STATIC ${FUSE_LITE_SRC})
target_include_directories(libfuse-lite PUBLIC
        ${CMAKE_SOURCE_DIR}/app
        ${CMAKE_SOURCE_DIR}/app/include/fuse-lite
)
set_target_properties(libfuse-lite PROPERTIES OUTPUT_NAME "libfuse-lite")
