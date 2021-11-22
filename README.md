# SLAM
###### link : http://wiki.ros.org/rtabmap_ros/Tutorials/HandHeldMapping
### LeTWC-520
##### git clone https://github.com/orbbec/ros_astra_camera.git
##### git clone https://github.com/orbbec/ros_astra_launch.git โหลดไฟล์ robot/SLAM : file ros_astra_launch เเทน
###### 1.install 
```
sudo apt install ros-*-rgbd-launch ros-*-libuvc ros-*-libuvc-camera ros-*-libuvc-ros
```
###### 3.install openni2,openni
###### 2.install
```
roscd astra_camera
./scripts/create_udev_rules
```
```
 <node pkg="astra_camera" type="camera_node" name="$(arg camera)_rgb">
      <!-- Parameters used to find the camera -->
      <param name="vendor" value="0x2bc5"/>
      <param name="product" value="0x0502"/>
      <param name="serial" value="0"/>
      <!-- If the above parameters aren't unique, choose the first match: -->
      <param name="index" value="$(arg index)"/>
```
RUN
```
roslaunch astra_launch astrapro.launch
```
```
roslaunch rtabmap_ros rtabmap.launch rtabmap_args:="--delete_db_on_start" rgb_topic:=/camera/rgb/image_raw depth_topic:=/camera/depth/image camera_info_topic:=/camera/depth/camera_info approx_sync:=true frame_id:=camera_link
```
