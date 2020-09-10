## Robotics projects involving RViz, Gazebo and ROS
This repository is dedicated to showcasing some of my major and mini-Robotics projects done as a part of courseware and Robotics Nanodegree. Each project has links to its corresponding project repo and README.

#### 1. [RANSAC plane fitting using PCL](#RANSAC-plain-fitting-using-PCL)
#### 2. [Image Segmentation using PCL](#Image-Segmentation-using-PCL)
#### 3. [Object Recognition and Labelling](#Object-Recognition-and-Labelling)
#### 4. [PR2-Robot 3D Perception and Control](#PR2-Robot-3D-Perception-and-Control)
#### 5. [Ball Chaser using ROS Kinetic Navigation](#Ball-Chaser-using-ROS-Kinetic-Navigation)
#### 6. [Map the Robot World using SLAM and RTAB-MAP](#Map-the-Robot-World-using-SLAM-and-RTAB-MAP)

## RANSAC plane fitting using PCL

This project uses the  [Point Cloud Library](https://pointclouds.org/) (PCL). PCL is open project for 2D/3D image and point cloud processing. The PCL API documentation [here](https://pointclouds.org/documentation/) , contains details of implementing many state-of-the-art algorithms using filtering , feature estimation, surface reconstruction and segmentation.

The project comprises of using the "RANdom SAmple Consensus" ([RANSAC](http://wiki.ros.org/pcl/Handbook/RANSAC)) algorithm to create point-clouds of random objects/things kept on a cluttered table.A successful implementation of the algorithm results in creating new point clouds containing the table and objects separately. The README corresponding to the project repo briefly explains the process and the filtering technique used, more can be found here - [python-pcl](https://python-pcl-fork.readthedocs.io/en/rc_patches4/tutorial/filtering.html#filtering-a-pointcloud-using-a-passthrough-filter).

#### Click 👉 for [Project Details](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/tree/master/ransac_pointcloud)

<img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/voxel.png" height="425px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/pass_through.png" height="425px" width="400px"/>


<img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/tabletop.png" height="425px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/ransac_pointcloud/extracted_in.png" height="425px" width="400px"/>


## Image Segmentation using PCL
The project creates a [ROS Node](http://wiki.ros.org/ROS/Tutorials/UnderstandingNodes) for image segmentation for objects kept on the cluttered table from the `pcd`'s used in the RANSAC plane fitting project above. The setup is run and tested on the RoboND simulator Environment provided by Udacity. The segmentation has been visualized in `Rviz` by selecting the `/pcl_objects` topic.
A successful implementation of the cluster based segmentation using [Voxel Grid filtering](https://python-pcl-fork.readthedocs.io/en/rc_patches4/tutorial/filtering.html#downsampling-a-pointcloud-using-a-voxelgrid-filter) results in assigning a different colour to each custer.

The `Gazebo` setup for the same table top consists of a stick robot with an RBG-D camera attached to its head.  

#### Click 👉 for  [Project Details](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation#Image-Segmentation)


<img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/sensor_stick/pcl1.png" height="425px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/sensor_stick/pcl2.png" height="425px" width="400px"/>

## Object Recognition and Labelling
This project uses scripts and concepts from RANSAC plane fitting and Image segmentation to ultimately recognize objects on the cluttered table. A SVM classifier is trained to detect the objects kept on the cluttered table.

#### Click 👉 for  [Project Details](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation#Object-Recognition-and-Labelling)

<p align="center">
<img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/object_recognize/obj_recognize.png"/>
</p>

## PR2-Robot 3D Perception and Control
This project gives the [PR2 robot](https://robots.ieee.org/robots/pr2/) the ability to locate an object in a cluttered environment, pick it up and then move it to some other location. This is an interesting problem to solve and is a challenge at the forefront of the robotics industry today. The project uses a perception pipeline , [here](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation#Image-Segmentation) and [here](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation#Object-Recognition-and-Labelling), to identify target objects from a so-called “Pick-List” in that particular order, pick up those objects and place them in corresponding drop-boxes.

Performing image segmentation and object detection are two important parts of the project forming the perception pipeline for the PR2 Robot. The control/Actuator part is handled by calling a `PR2 mover function`, which then calls the `pr2_mover` to pick and place detected objects.
The project deals with three test world scenarios one of whose results is shown in the below image

#### Click 👉 for  [Project Details](https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception)

<img src="https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception/blob/master/pr2_robot/run/world3.jpg" height="350px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception/blob/master/pr2_robot/run/obj3.png" height="350px" width="380px"/>

## Ball Chaser using ROS Kinetic Navigation

#### Click 👉 for  [Project Details](https://github.com/ashutoshtiwari13/Map-a-world-with-SLAM/tree/master/GochaseIt)


## Map the Robot World using SLAM and RTAB-MAP

#### Click 👉 for  [Project Details](https://github.com/ashutoshtiwari13/Map-a-world-with-SLAM)
