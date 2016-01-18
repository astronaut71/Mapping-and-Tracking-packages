cmake_minimum_required(VERSION 2.4.6)
include($ENV{ROS_ROOT}/core/rosbuild/rosbuild.cmake)

find_package(Qt4 COMPONENTS QtCore QtGui)
INCLUDE(${QT_USE_FILE})
ADD_DEFINITIONS(${QT_DEFINITIONS})


# Set the build type.  Options are:
#  Coverage       : w/ debug symbols, w/o optimization, w/ code-coverage
#  Debug          : w/ debug symbols, w/o optimization
#  Release        : w/o debug symbols, w/ optimization
#  RelWithDebInfo : w/ debug symbols, w/ optimization
#  MinSizeRel     : w/o debug symbols, w/ optimization, stripped binaries
#set(ROS_BUILD_TYPE RelWithDebInfo)


rosbuild_init()

#set the default path for built executables to the "bin" directory
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#set the default path for built libraries to the "lib" directory
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

#uncomment if you have defined messages
rosbuild_genmsg()
#uncomment if you have defined services
#rosbuild_gensrv()

#common commands for building c++ executables and libraries
#rosbuild_add_library(${PROJECT_NAME} src/example.cpp)
#target_link_libraries(${PROJECT_NAME} another_library)
#rosbuild_add_boost_directories()
#rosbuild_link_boost(${PROJECT_NAME} thread)
#rosbuild_add_executable(example examples/example.cpp)
#target_link_libraries(example ${PROJECT_NAME})

#rosbuild_add_executable(pida_door_bed src/pida_door_bed.cpp)
#rosbuild_add_executable(wst_forward_10m_asses_kopija src/wst_forward_10m_asses_kopija.cpp)
rosbuild_add_executable(wst_forward10m_raw_assess src/wst_forward10m_raw_assess.cpp)
#rosbuild_add_executable(pida_turn_180deg_window_asses src/pida_turn_180deg_window_asses.cpp)
#rosbuild_add_executable(pida_beside_parking_asses src/pida_beside_parking_asses.cpp)
#rosbuild_add_executable(test_qt src/test_qt.cpp)
rosbuild_add_executable(pida_turn_180deg_asses src/pida_turn_180deg_asses.cpp)
#rosbuild_add_executable(pida_ramp_up_asses src/pida_ramp_up_asses.cpp)
rosbuild_add_executable(pida_ramp_down_asses src/pida_ramp_down_asses.cpp)
#rosbuild_add_executable(wst_turn_90deg_asses src/wst_turn_90deg_asses.cpp)
#rosbuild_add_executable(wst_forward_10m_asses src/wst_forward_10m_asses.cpp)
#rosbuild_add_executable(pida_parallel_parking_asses src/pida_parallel_parking_asses.cpp)
#rosbuild_add_executable(pida_turn_hallway_asses2 src/pida_turn_hallway_asses2.cpp)
#rosbuild_add_executable(pida_intersection_asses src/pida_intersection_asses.cpp)
#rosbuild_add_executable(pida_backward_asses src/pida_backward_asses.cpp)
#rosbuild_add_executable(pida_turn_hallway_asses1 src/pida_turn_hallway_asses1.cpp)
#rosbuild_add_executable(pida_ramp_3d_asses src/pida_ramp_3d_asses.cpp)
#rosbuild_add_executable(pida_ramp_asses src/pida_ramp_asses.cpp)
#rosbuild_add_executable(ramp_assess src/ramp_assess.cpp)
#rosbuild_add_executable(damn src/damn.cpp)
rosbuild_add_executable(scan_conv src/scan_fix.cpp)
#rosbuild_add_executable(tf_fix_gmapping src/tf_fix_gmapping.cpp)
rosbuild_add_executable(converter src/converter.cpp)
rosbuild_add_executable(converter_ekf src/converter_ekf.cpp)
#rosbuild_add_executable(object_node src/object_node.cpp)
rosbuild_add_executable(doors_node src/doors_node.cpp)
rosbuild_add_executable(beds_node src/beds_node.cpp)
rosbuild_add_executable(hector_odometry src/hector_odometry.cpp)
rosbuild_add_executable(speed_node_mod src/speed_node_mod.cpp)
rosbuild_add_executable(speed_node_hector src/speed_node_hector.cpp)
rosbuild_add_executable(speed_node src/speed_node.cpp)
rosbuild_add_executable(speed_node_amcl src/speed_node_amcl.cpp)
rosbuild_add_executable(ekf_odom src/ekf_odom.cpp)
#rosbuild_add_executable(imu_odom src/imu_odom.cpp)
rosbuild_add_executable(amcl_odom src/amcl_odom.cpp)
#rosbuild_add_executable(position_segway src/position_segway.cpp)
rosbuild_add_executable(ekf_odom_timestamp src/ekf_odom_timestamp.cpp)
#rosbuild_add_executable(odom_split src/odom_split.cpp)
rosbuild_add_executable(ekf_repub src/ekf_repub.cpp)

#target_link_libraries(test_qt ${QT_LIBRARIES})

