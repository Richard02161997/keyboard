cmake_minimum_required(VERSION 2.8.3)
project(keyboard)


find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES keyboard
#  CATKIN_DEPENDS geometry_msgs roscpp
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)


add_executable(telep_keyboard src/telep_keyboard.cpp)


add_dependencies(telep_keyboard  ${catkin_EXPORTED_TARGETS})

target_link_libraries(telep_keyboard
  ${catkin_LIBRARIES}
)


