## Run
   - Launch zed node to publish pointcloud topic
   ```Shell
   roslaunch zed_wrapper zed_pointcloud.launch
   ```

## Configure
   - Modify parameters in `zed_wrapper/params/common.yaml`
   ```Shell
   depth:
       quality: 2 #QUALITY
       sensing_mode: 1 #FILL
       depth_stablilization: 1
       openni_depth_mode: false
       depth_downsample_factor: 0.25 #Set 1 if don't downsample
   pos_tracking:
       publish_tf: true
       publish_map_tf: true
   mapping:
       mapping_enabled: false
   ```
   
## Record
   - Record data of pointcloud
   ```Shell
   rosbag record /image_rectified /zed/zed_node/point_cloud/cloud_registered /tf /tf_static
   ```
