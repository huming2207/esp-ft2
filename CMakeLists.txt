idf_component_register()

set(FT_DISABLE_ZLIB TRUE CACHE BOOL "Override option" FORCE)
set(FT_DISABLE_BZIP2 TRUE CACHE BOOL "Override option" FORCE)
set(FT_DISABLE_PNG TRUE CACHE BOOL "Override option" FORCE)
set(FT_DISABLE_HARFBUZZ TRUE CACHE BOOL "Override option" FORCE)
set(FT_DISABLE_BROTLI TRUE CACHE BOOL "Override option" FORCE)

# No need to install and export
function(install)
endfunction()

function(export)
endfunction()

add_subdirectory(freetype)

target_link_libraries(${COMPONENT_LIB} INTERFACE freetype)