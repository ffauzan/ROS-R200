# Intel Realsense camera C++ application for ROS.

This package have been tested in ROS kinetic only and no guarantee for other ROS versions.

## Device support

Intel realsense R200 camera

## Pre-install & Requirements
Note that all packages should be installed in path /opt/... or the catkin tool cant find them!

 1. [ROS install](http://wiki.ros.org/kinetic/Installation/Ubuntu)

 ```
 sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
 sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
 sudo apt-get update
 sudo apt-get -y install ros-kinetic-desktop-full
 sudo rosdep init
 rosdep update
 echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
 source ~/.bashrc
 ```

 2. [librealsense](https://github.com/IntelRealSense/realsense_samples_ros#installation-instructions)

 ```
 sudo apt-key adv --keyserver keys.gnupg.net --recv-key D6FB2970
 sudo sh -c 'echo "deb http://realsense-alm-public.s3.amazonaws.com/apt-repo xenial main" > /etc/apt/sources.list.d/realsense-latest.list'
 sudo apt update
 sudo apt install -y librealsense-object-recognition-dev librealsense-persontracking-dev librealsense-slam-dev libopencv-dev
 ```
 3. realsense-camera
	
  ```
  sudo apt-get install ros-kinetic-realsense-camera
  ```	
 4. OpenCV greater than 3.2.0 version

## How to use this package?

Assume that you alredy have a catkin-workspace (`catkin_ws`) in your root directory.
```
cd ~/catkin_ws/src
git clone https://github.com/EdXian/ROS-R200.git
cd ..
catkin_make

```
## Reference and Cookbook
 * [OpenCV3.2 tutorial](https://docs.opencv.org/3.2.0/d9/d97/tutorial_table_of_content_features2d.html)
 * [Stream Format](https://github.com/IntelRealSense/librealsense/blob/legacy/doc/supported_video_formats.pdf)
 * [Step by Step](https://software.intel.com/en-us/articles/using-librealsense-and-opencv-to-stream-rgb-and-depth-data#_Toc462147826)
 * [Developer's Guide](https://software.intel.com/sites/products/realsense/camera/developer_guide.html)

## TODO List
 * Object-tracking in real-time.
 * SLAM (Simultaneous localiztion and mapping)

