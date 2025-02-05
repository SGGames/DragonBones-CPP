project(DBSFMLDemo)

add_executable(DemoAnimationLayer AnimationLayer/AnimationLayer.cpp)
add_executable(DemoDragonBoy HelloDragonBones/DragonBoy.cpp)

include_directories(${Rapidjson_INCLUDE_DIRS})
include_directories(${SFML_INCLUDE_DIRS})
include_directories(${DRAGONBONES_INCLUDE_DIRS})
include_directories(${DBSFML_INCLUDE_DIRS})

target_link_libraries(DemoAnimationLayer PRIVATE sfml-graphics sfml-window sfml-system DragonBones DBSFML)
target_link_libraries(DemoDragonBoy PRIVATE sfml-graphics sfml-window sfml-system DragonBones DBSFML)