# SLAM
###### link : http://wiki.ros.org/rtabmap_ros/Tutorials/HandHeldMapping
### LeTWC-520
##### git clone https://github.com/orbbec/ros_astra_camera.git
##### git clone https://github.com/orbbec/ros_astra_launch.git โหลดไฟล์เเทน robot/SLAM : file ros_astra_launch
เเก้ไข ros_astra_launch/launch/astra.launch
```
<node pkg="uvc_camera" type="uvc_camera_node" name="uvc_camera" output="screen" 	/>
<param name="width" type="int" value="320" />
<param name="height" type="int" value="240" />
<param name="fps" type="int" value="30" />
<param name="frame" type="string" value="wide_stereo" />

<param name="auto_focus" type="bool" value="False" />
<param name="focus_absolute" type="int" value="0" />
<!-- other supported params: auto_exposure, exposure_absolute, brightness, power_line_frequency -->

<param name="device" type="string" value="/dev/video0" /> 
<param name="camera_info_url" type="string" value="file://$(find uvc_camera)/example.yaml" />

```
RUN
```
roslaunch astra_launch astrapro.launch
```
```
roslaunch rtabmap_ros rtabmap.launch rtabmap_args:="--delete_db_on_start" rgb_topic:=/camera/rgb/image_raw depth_topic:=/camera/depth/image_rect_raw camera_info_topic:=/camera/depth/camera_info frame_id:=camera_link
```
