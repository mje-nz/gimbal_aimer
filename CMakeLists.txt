cmake_minimum_required(VERSION 2.8.3)
project(gimbal_aimer)

find_package(catkin REQUIRED COMPONENTS rospy python_natnet)

## Uncomment this if the package has a setup.py. This macro ensures
## modules and global scripts declared therein get installed
## See http://ros.org/doc/api/catkin/html/user_guide/setup_dot_py.html
# catkin_python_setup()

catkin_package(CATKIN_DEPENDS rospy)

catkin_install_python(PROGRAMS scripts/aimer DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY test_data DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
    FILES_MATCHING PATTERN "*.bag")
