file(GLOB SOURCE_FILES *.cpp)
file(GLOB HEADER_FILES *.h)

include_directories(${SDL_INCLUDE_DIR})

add_executable(example_cube ${SOURCE_FILES} ${HEADER_FILES})
target_link_libraries(example_cube LINK_PUBLIC nano3d nano3d_ex ${SDL_LIBRARY})

set_target_properties(example_cube PROPERTIES
    FOLDER examples
)
