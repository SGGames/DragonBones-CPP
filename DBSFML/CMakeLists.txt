project(DBSFML)

file(GLOB_RECURSE SRCS *.cpp)

find_package(SFML COMPONENTS system window graphics CONFIG REQUIRED)
find_package(rapidjson CONFIG REQUIRED)

include_directories(${Rapidjson_INCLUDE_DIRS})
include_directories(${SFML_INCLUDE_DIRS})
include_directories(${DRAGONBONES_INCLUDE_DIRS})

add_library(DBSFML ${SRCS})

target_link_libraries(DBSFML PRIVATE sfml-graphics sfml-window sfml-system DragonBones)
target_include_directories(DBSFML PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/src")