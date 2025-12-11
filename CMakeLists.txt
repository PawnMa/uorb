set(COMPONENT_NAME uorb)
set(CMAKE_CXX_STANDARD 17)

file(GLOB_RECURSE UORB_SOURCES
        "src/base/orb_errno.cc"
        "src/device_master.cc"
        "src/device_node.cc"
        "src/uorb.cc"
)
set(UORB_INC 
        "include"
        "src"
        "src/base"
        "src/base/intrusive_list")

idf_component_register(SRCS ${UORB_SOURCES}
        INCLUDE_DIRS "include"
        PRIV_INCLUDE_DIRS ${UORB_INC})