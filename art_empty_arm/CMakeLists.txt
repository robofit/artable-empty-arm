cmake_minimum_required(VERSION 2.8.3)
project(art_empty_arm)

find_package(catkin REQUIRED COMPONENTS
    roslaunch
    )

catkin_package()

if (CATKIN_ENABLE_TESTING)
  roslaunch_add_file_check(launch)
endif()

install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch)
