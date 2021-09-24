# SLAM
###### link : http://wiki.ros.org/rtabmap_ros/Tutorials/HandHeldMapping
### LeTWC-520
```
roslaunch rtabmap_ros rtabmap.launch rtabmap_args:="--delete_db_on_start" rgb_topic:=/camera/rgb/image_raw depth_topic:=/camera/depth/image_rect_raw    camera_info_topic:=/camera/depth/camera_info frame_id:=camera_link
```
