file(GLOB_RECURSE ALL_SRC
    *.cpp
)

add_library(core SHARED ${ALL_SRC})

target_include_directories(core PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/app
)
