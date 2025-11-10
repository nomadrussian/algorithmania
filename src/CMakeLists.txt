add_subdirectory(core)
add_subdirectory(cli)
add_subdirectory(gui)

#include(GNUInstallDirs)
#install(TARGETS algorithmania
#    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
#    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
#)
