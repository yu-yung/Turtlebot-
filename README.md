# Turtlebot-multi-navigation

cd ~/catkin_ws/src/multinav/src
touch nav.py

需事先存好地圖於指定路徑 Example:
/home/map/home.yaml

點擊RVIZ工具欄上的Publish point，移到地圖上的任意點，查看左下角的座標點 x,y,z 。

座標點字典 Example:
locations['home_cafe'] = Pose(Point(x, y, z), Quaternion(0.000, 0.000, 0.000, 1.000)) 

roslaunch turtlebot_bringup minimal.launch

roslaunch turtlebot_navigation amcl_demo.launch map_file:=/home/map/home.yaml 

roslaunch turtlebot_rviz_launchers view_navigation.launch

rosrun multinav nav.py
