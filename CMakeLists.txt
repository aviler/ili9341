# include paths of this components.
set(COMPONENT_ADD_INCLUDEDIRS main)

# source files of this components.
# set(COMPONENT_SRCDIRS src)
# Alternatively, use COMPONENT_SRCS to specify source files explicitly
set(COMPONENT_SRCS main/fontx.c main/ili9340.h)

# add this components, this will define a CMake library target.
register_component()

# standard CMake function can be used to specify dependencies. ${COMPONENT_TARGET} is defined
# from esp-idf when you call register_component, by default it's idf_component_<folder_name>.
target_link_libraries(${COMPONENT_TARGET} PRIVATE idf_component_spiffs)
