# Avi to Rosbag file in ROS

A simple description of converting video files to ROS bagfiles.

## 

## Video to Bagfile

1. Install [ROS Kinetic](http://wiki.ros.org/kinetic/Installation/Ubuntu) on Ubuntu.
2. Use catkin or any build system.
3. Download [video_stream_opencv](https://github.com/ros-drivers/video_stream_opencv). Go to the launch folder of [video_stream_opencv](https://github.com/ros-drivers/video_stream_opencv) and open video_file.launch. Then, add the avi file path to the value section of "video_stream_provider".
4. Build [video_stream_opencv](https://github.com/ros-drivers/video_stream_opencv).
5. In a new terminal, run roscore. Then, run this command: roslaunch video_stream_opencv video_file.launch 
6. Open a new terminal, run this command: rosbag record -O filename /videofile/image_raw

## Additional Information
Add source install_isolated/setup.bash in .bashrc. Run source ~/.bashrc
.bag files are very large.

After running the video by video_stream_opencv, run this command to see active nodes: rostopic list -v
/videofile/image_raw is a node.

For more information:

http://wiki.ros.org/ROS/Tutorials/Recording%20and%20playing%20back%20data
 
