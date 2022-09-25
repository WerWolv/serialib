project(libserialib)

if (SERIALIB_BUILD_SHARED_LIBRARY)
    set(LIBRARY_TYPE SHARED)
else()
    set(LIBRARY_TYPE STATIC)
endif ()

add_library(libserialib ${LIBRARY_TYPE}
        source/serialib.cpp
)

target_include_directories(libserialib PUBLIC include)
set_target_properties(libserialib PROPERTIES PREFIX "")