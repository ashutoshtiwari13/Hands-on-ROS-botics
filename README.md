## Robotics projects involving ROS
This repository is dedicated to showcasing some of my major and mini-Robotics projects done as a part of courseware and Robotics Nanodegree. Each project has links to its corresponding project repo and README.

#### 1. [RANSAC plane fitting using PCL](#RANSAC-plain-fitting-using-PCL)
#### 2. [Image Segmentation using PCL](#Image-Segmentation-using-PCL)
#### 3. [Object Recognition and Labelling](#Object-Recognition-and-Labelling)
#### 4. [PR2-Robot 3D Perception and Control](#PR2-Robot-3D-Perception-and-Control)
#### 5. [Ball Chaser using ROS Kinetic Navigation](#Ball-Chaser-using-ROS-Kinetic-Navigation)
#### 6. [Map the Robot World using SLAM and RTAB-MAP](#Map-the-Robot-World-using-SLAM-and-RTAB-MAP)

## RANSAC plane fitting using PCL

This project uses the  [Point Cloud Library](https://pointclouds.org/) (PCL). PCL is open project for 2D/3D image and point cloud processing. The PCL API documentation [here](https://pointclouds.org/documentation/) , contains details of implementing many state-of-the-art algorithms using filtering , feature estimation, surface reconstruction and segmentation.

The project comprises of using the "RANdom SAmple Consensus" ([RANSAC](http://wiki.ros.org/pcl/Handbook/RANSAC)) algorithm to create point-clouds of random objects/things kept on a cluttered table.A successful implementation of the algorithm results in creating new point clouds containing the table and objects separately. The README corresponding to the project repo briefly explains the process and the filtering technique used, more can be found - [python-pcl](https://python-pcl-fork.readthedocs.io/en/rc_patches4/tutorial/filtering.html#filtering-a-pointcloud-using-a-passthrough-filter).

<img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/voxel.png" height="425px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/pass_through.png" height="425px" width="400px"/>


<img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/tabletop.png" height="425px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/extracted_in.png" height="425px" width="400px"/>


## Image Segmentation using PCL

## Object Recognition and Labelling

## PR2-Robot 3D Perception and Control

## Ball Chaser using ROS Kinetic Navigation

## Map the Robot World using SLAM and RTAB-MAP
