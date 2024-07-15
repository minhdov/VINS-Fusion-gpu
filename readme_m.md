# Reference: 
https://github.com/pjrambo/VINS-Fusion-gpu
https://github.com/IOdissey/VINS-Fusion-GPU

# RUN VIN-FUSION with Videos
### 3.1 Monocualr camera + IMU

```
    source ~/catkin_ws_gpu_ba_cpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion/config/euroc/euroc_mono_imu_config.yaml 

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion/config/euroc/euroc_mono_imu_config.yaml 

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```

### 3.2 Stereo cameras + IMU

```
    source ~/catkin_ws_gpu_ba_cpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config.yaml

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config.yaml

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
### 3.2.2 Stereo cameras + IMU - Tiny

```
    source ~/catkin_ws_gpu_ba_cpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny.yaml

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny.yaml

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
### 3.2.3 Stereo cameras + IMU - Tiny50

```
    source ~/catkin_ws_gpu_ba_cpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny50.yaml

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny50.yaml

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
### 3.3 Stereo cameras

```
    source ~/catkin_ws_gpu_ba_cpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion/config/euroc/euroc_stereo_config.yaml 

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion/config/euroc/euroc_stereo_config.yaml 

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
# RUN VIN-FUSION with Camera

### 3.4 VINS-FUSION with realsense camera 640x480

source ~/catkin_ws_gpu_ba_cpu/devel/setup.bash

roslaunch vins vins_rviz.launch

roslaunch realsense2_camera rs_camera_2.launch  

rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config.yaml 

rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config.yaml 

roslaunch surfel_fusion vins_realsense.launch

### 3.4.1 VINS-FUSION with realsense camera tiny75

rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny75.yaml 

rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny75.yaml 

### 3.4.1 VINS-FUSION with realsense camera tiny50

rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny50.yaml 

rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny50.yaml 
*************************************************************
## VINS-FUSION with realsense camera 1280x720
### 3.5 VINS-FUSION with realsense camera 1280x720

source ~/catkin_ws_gpu_ba_cpu/devel/setup.bash

roslaunch vins vins_rviz.launch

roslaunch realsense2_camera rs_camera_720p.launch  

rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_720p.yaml 

rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_720p.yaml 

### 3.4.1 VINS-FUSION with realsense camera tiny75

rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny75.yaml 

rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny75.yaml 

### 3.4.1 VINS-FUSION with realsense camera tiny50

rosrun vins vins_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny50.yaml 

rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu_ba_cpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config_tiny50.yaml 
*************************************************************
# Date 20240418
- Launch octomap:  roslaunch octomap_integration octomap_mapping.launch
 roslaunch octomap_server octomap_mapping.launch

 # Date 20240423
 roslaunch surfel_fusion vins_realsense.launch
 roslaunch fiesta D435i.launch



[ERROR] [1713860584.546258899]: PluginlibFactory: The plugin for class 'rviz_plugins/Goal3DTool' failed to load.  Error: According to the loaded plugin descriptions the class rviz_plugins/Goal3DTool with base class type rviz::Tool does not exist. Declared types are  rviz/FocusCamera rviz/Interact rviz/Measure rviz/MoveCamera rviz/PublishPoint rviz/Select rviz/SetGoal rviz/SetInitialPose rviz_plugin_tutorials/PlantFlag
[rospack] Error: no pa

rviz_visual_tools/RvizVisualToolsMap

rviz_plugin_tutorials/Teleop rviz_visual_tools/RvizVisualToolsGui

