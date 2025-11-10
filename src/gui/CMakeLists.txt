find_package(Qt6 REQUIRED COMPONENTS Core Gui Widgets)
qt_standard_project_setup()

file(GLOB ALL_SRC
    *.cpp
    app/*.cpp
)

qt_add_executable(algorithmania-gui ${ALL_SRC})

target_link_libraries(algorithmania-gui PRIVATE
    Qt6::Core
    Qt6::Gui
    Qt6::Widgets
    core
)

target_include_directories(algorithmania-gui PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/app
)
