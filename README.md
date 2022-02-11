# Robot Pose EKF
Takes IMU, Visual Odometry (and eventually wheel odometry) to provide localization.

# How to use it Simulation
- roslaunch hhcm_perception centauro_world_sim.launch sim:=false  (so that T625 does not move the robot frames)
- xbot2-core --simtime
- rosservice call /xbotcore/homing/switch 1
- roslaunch robot_pose_ekf robot_pose_ekf.launch
- rosrun hhcm_perception attach_odom

