# Reference: 
https://github.com/pjrambo/VINS-Fusion-gpu
https://github.com/IOdissey/VINS-Fusion-GPU

# RUN VIN-FUSION
### 3.1 Monocualr camera + IMU

```
    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws/src/VINS-Fusion/config/euroc/euroc_mono_imu_config.yaml 

    rosrun loop_fusion loop_fusion_node ~/catkin_ws/src/VINS-Fusion/config/euroc/euroc_mono_imu_config.yaml 

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```

### 3.2 Stereo cameras + IMU

```
    source ~/catkin_ws_gpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config.yaml

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config.yaml

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
### 3.2.2 Stereo cameras + IMU - Tiny

```
    source ~/catkin_ws_gpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny.yaml

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny.yaml

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
### 3.2.3 Stereo cameras + IMU - Tiny50

```
    source ~/catkin_ws_gpu/devel/setup.bash

    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny50.yaml

    rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/euroc/euroc_stereo_imu_config_tiny50.yaml

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
### 3.3 Stereo cameras

```
    roslaunch vins vins_rviz.launch

    rosrun vins vins_node ~/catkin_ws/src/VINS-Fusion/config/euroc/euroc_stereo_config.yaml 

    rosrun loop_fusion loop_fusion_node ~/catkin_ws/src/VINS-Fusion/config/euroc/euroc_stereo_config.yaml 

    rosbag play YOUR_DATASET_FOLDER/MH_01_easy.bag
```
### 3.4 VINS-FUSION with realsense camera
source ~/catkin_ws_gpu/devel/setup.bash

roslaunch vins vins_rviz.launch

roslaunch realsense2_camera rs_camera_d435i.launch  

rosrun vins vins_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config.yaml 

rosrun loop_fusion loop_fusion_node ~/catkin_ws_gpu/src/VINS-Fusion-gpu/config/realsense_d435i/realsense_stereo_imu_config.yaml 

source ~/catkin_ws/devel/setup.bash
****************************************************************************************************
# Date: 20240409 
# References
https://github.com/qdLMF/VINS-Fusion-GPU-BA

# Purpose
- Integrate VINS-FUSION BA GPU to VINS-Fusion GPU