#set(COMPONENT_SRCDIRS src 
#                      src/Fonts
#                      src/utility)

#set(COMPONENT_ADD_INCLUDEDIRS src)

#set(COMPONENT_PRIV_INCLUDEDIRS src/Fonts 
#                               src/Fonts/Custom 
#                               src/Fonts/GFXFF 
#                               src/Fonts/TrueType 
#                               src/utility)

#set(COMPONENT_REQUIRES arduino)
#set(COMPONENT_PRIV_REQUIRES arduino)

#register_component()
idf_component_register(SRC_DIRS src src/Fonts src/Utility INCLUDE_DIRS src PRIV_INCLUDE_DIRS src/Fonts src/Fonts/Custom src/Fonts/GFXFF src/Fonts/TrueType src/utility PRIV_REQUIRES arduino arduino)
set_property(TARGET ${COMPONENT_LIB} APPEND PROPERTY LINK_INTERFACE_MULTIPLICITY 3)
