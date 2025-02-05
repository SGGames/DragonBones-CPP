cmake_minimum_required(VERSION 3.10)

project(DragonBonesCPP)

find_package(SFML COMPONENTS system window graphics CONFIG REQUIRED)
find_package(rapidjson CONFIG REQUIRED)

include_directories(${Rapidjson_INCLUDE_DIRS})

add_subdirectory(DragonBones)
add_subdirectory(DBSFML)
add_subdirectory(DBSFMLDemo)