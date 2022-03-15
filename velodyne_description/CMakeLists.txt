cmake_minimum_required(VERSION 3.5.0)
project(velodyne_description)

find_package(ament_cmake REQUIRED)

ament_environment_hooks(${CMAKE_CURRENT_SOURCE_DIR}/env-hooks/72.velodyne_description.dsv.in)

ament_package()

install(DIRECTORY launch/
  DESTINATION share/${PROJECT_NAME}/launch
)

install(DIRECTORY meshes/
  DESTINATION share/${PROJECT_NAME}/meshes
)

install(DIRECTORY rviz/
  DESTINATION share/${PROJECT_NAME}/rviz
)

install(DIRECTORY urdf/
  DESTINATION share/${PROJECT_NAME}/urdf
)

install(DIRECTORY world/
  DESTINATION share/${PROJECT_NAME}/world
)
