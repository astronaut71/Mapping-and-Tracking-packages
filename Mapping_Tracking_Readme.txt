1.Map Building

1.1 PoW

Map building of PoW using Hector Mapping. Install hector_mapping package. Load pow_ros_extra_2011-04-01-15-16-03.bag bag file for the launch file. Launch the pow_analyze_hector_pow.launch launch file with: roslaunch pow_analyze_hector_pow.launch launch. Run the map_server ROS Node after the launch file created the map using the command "rosrun map_server map_saver -f map_name". 

1.2 UTS Level 2

Map building of UTS Level2 using Hector Mapping. Install hector_mapping package. Load uts_level2.bag bag file for the launch file. Launch the pow_analyze_hector_uts_level2.launch launch file with: roslaunch pow_analyze_hector_uts_level2.launch. Run the map_server ROS Node after the launch file created the map using the command "rosrun map_server map_saver -f map_name". 

1.3 GDS

Map building of GDS environment using Hector Mapping. Install hector_mapping package. Load gds.bag bag file for the launch file. Launch the pow_analyze_hector_gds.launch launch file with:roslaunch pow_analyze_hector_gds.launch launch . Run the map_server ROS Node after the launch file created the map using the command "rosrun map_server map_saver -f map_name". 

2. Pose

2.1 PoW

Pose recording of PoW using the Hector Mapping. Install hector_mapping package. Run the pow_analyze_hector_pow.launch launch file with the arg:=/slam_out_pose (roslaunch pow_analyze_hector_pow.launch arg:=/slam_out_pose). In the new tab terminal run the command: xdg-open ~/.ros. Then in run the command: rostopic echo -b ~/.ros/bag_file_name.bag -p /slam_out_pose > file_name.csv

Pose recording of PoW using AMCL. Run the pow_analyze_amcl_pow.launch launch file with the arg:=/amcl_pose (roslaunch pow_analyze_hector_pow.launch arg:=/amcl_pose). In the new tab terminal run the command: xdg-open ~/.ros. Then run the command rostopic echo -b ~/.ros/bag_file_name.bag -p /amcl_pose > file_name.csv

2.2 UTS Level 2

Pose recording of UTS Level 2 using the Hector Mapping. Install hector_mapping ROS package. Run the pow_analyze_hector_uts_level2.launch launch file with the arg:=/slam_out_pose (roslaunch pow_analyze_hector_uts_level2.launch arg:=/slam_out_pose). In the new tab terminal run the command: xdg-open ~/.ros. Then in run the command: rostopic echo -b ~/.ros/bag_file_name.bag -p /slam_out_pose > file_name.csv

Pose recording of UTS Level 2 using AMCL. Run the pow_analyze_amcl_wheelchair launch file with the arg:=/amcl_pose (roslaunch pow_analyze_amcl_wheelchair arg:=/amcl_pose). In the new tab terminal run the command: xdg-open ~/.ros. Then run the command rostopic echo -b ~/.ros/bag_file_name.bag -p /amcl_pose > file_name.csv

Pose recording of UTS Level 2 using EKF. Install Robot Pose EKF ROS package. Run the pow_analyze_hector_wheelchair_ekf_pose.launch file with the arg:=/robot_pose_ekf/odom_combined (roslaunch pow_analyze_hector_wheelchair_ekf_pose.launch arg:=/robot_pose_ekf/odom_combined). In the new tab terminal run the command: xdg-open ~/.ros. Then run the command rostopic echo -b ~/.ros/bag_file_name.bag -p /robot_pose_ekf > file_name.csv




