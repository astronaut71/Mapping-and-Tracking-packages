1. Alignment with Beds

Run the pow_analyze_beds_doors launch file 

2. Minimum distance to Doors

Run the pow_analyze_beds_doors launch file 

3. Velocity Profiles

3.1 PoW Velocity Profiles
 
Velocity Profiles of PoW using Hector Mapping. Install hector_mapping package. Load all Pow bag files for the launch file (from User 1 to User4) into the pow_analyze "data" folder. Launch the pow_analyze_hector_pow.launch launch file with the argument in: node name="rosplay" pkg="rosbag" type="play" args="$(find pow_analyzer)/data/"name of the bag file from User 1 to User 4"

3.2 UTS Level 2 Velocity Profiles

Velocity Profiles of UTS Level2 using Hector Mapping. Install hector_mapping package. Launch the pow_analyze_hector_speed.launch launch file. 

Velocity Profiles of UTS Level2 using AMCL. Launch the pow_analyze_amcl_wheelchair.launch launch file. (with the follwing launch argument: <node pkg="pow_analyzer" type="speed_node_amcl" name="speed_node_amcl" output="screen"/> 	)

Velocity Profiles of UTS Level2 fusing virtual odometry from Hector Mapping and IMU. Install hector_mapping package. Istall robot_pose_ekf ROS Package. Launch the pow_analyze_wc_ekf_imu_hector.launch launch file. 

Velocity Profiles of UTS Level2 fusing raw odometry and IMU. Istall robot_pose_ekf ROS Package. Launch the pow_analyze_wc_ekf_imu_odom.launch launch file.


