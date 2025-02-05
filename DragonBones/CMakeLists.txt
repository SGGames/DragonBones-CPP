
project(DragonBones)

file(GLOB_RECURSE SRCS *.cpp)

find_package(rapidjson CONFIG REQUIRED)
find_package(SFML COMPONENTS system window graphics CONFIG REQUIRED)

include_directories(${Rapidjson_INCLUDE_DIRS})

add_library(DragonBones ${SRCS})

target_link_libraries(DragonBones PRIVATE sfml-graphics sfml-window sfml-system)
target_include_directories(DragonBones PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/src")