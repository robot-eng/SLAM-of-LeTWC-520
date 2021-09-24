# SLAM
###### link : http://wiki.ros.org/rtabmap_ros/Tutorials/HandHeldMapping
### LeTWC-520
##### git clone https://github.com/orbbec/ros_astra_camera.git
##### git clone https://github.com/orbbec/ros_astra_launch.git fix robot/SLAM : file ros_astra_launch
```
roslaunch astra_launch astrapro.launch
```
```
roslaunch rtabmap_ros rtabmap.launch rtabmap_args:="--delete_db_on_start" rgb_topic:=/camera/rgb/image_raw depth_topic:=/camera/depth/image_rect_raw camera_info_topic:=/camera/depth/camera_info frame_id:=camera_link
```
