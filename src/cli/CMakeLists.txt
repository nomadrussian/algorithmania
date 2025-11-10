# Using GLOB because it's a solo project and this is way less headache to do this
# than to list all the source files manually - it might be bad practice for team-based
# projects, but in this case (solo) it's way more efficient practically.
file(GLOB ALL_SRC
    *.cpp
    app/*.cpp
)

add_executable(algorithmania-cli ${ALL_SRC})

target_link_libraries(algorithmania-cli PRIVATE
    core
)

target_include_directories(algorithmania-cli PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/app
)
