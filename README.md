## Articubot by Articulated Robotics (Humble Version)

I'm also using [his GitHub template](https://github.com/joshnewans/my_bot).

---

Run Gazebo: ros2 launch articubot_humble launch_sim.launch.py world:=src/articubot_humble/worlds/obstacles.world

Run Rviz: ros2 run rviz2 rviz2 -d src/articubot_humble/config/main.rviz --ros-args -p use_sim_time:=true

Run teleop: ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped

Run slam_toolbox: ros2 launch slam_toolbox online_async_launch.py params_file:=./src/articubot_humble/config/mapper_params_online_async.yaml use_sim_time:=true

Run SLAM: ros2 launch articubot_humble online_async_launch.py use_sim_time:=true

Run Nav2: 
