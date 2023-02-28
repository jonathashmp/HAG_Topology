# Hybrid-Active-Gripper-A-Novel-Topology-for-Object-Grasping

This work presents a novel approach to object recognition using a reconfigurable gripper with multiple Time of Flight (ToF) sensors attached to in fingers and palm, introducing the concept of  Non-Contact Tactile Perception. The approach aims to promote the proprioceptive sense in the gripper workspace allowing the object prediction to manipulation tasks.

The Hybrid-Active (H-A) Gripper can adapt its topology to achieve an optimal pick-up and gripping over different objects, which requires a reliable object estimation. The Non-Contact Tactile Perception uses the ToF sensors and the gripper reconfiguration degrees-of-freedom for the 3D perception and surface estimation of pick-up object. The gripper is an active agent in the manipulation system because when the object is recognized by it, the gripper becomes the master assigning commands and goals to the manipulator. The method is based on five ToF sensors in the palm that identify the distance and adjust the gripper to the object's center through its capability of managing the manipulator.

The H-A Gripper also has twelve sensors distributed over its three fingers: four sensors on each finger, two on the distal phalanx, and two on the middle phalanx. Fingers have rotational mobility of 180º, allowing sensing of all faces of the object and at different angles to the tridimensional reconstruction. 
The proposed approach is evaluated in four experiments that analyze the influence of resolution, object complexity, finger tilt, and angular sampling over eleven objects with different complexities. The experimentation set allows the overall evaluation of Non-Contact Tactile Perception and the specification of its performance parameters.


Below we have the H-A Gripper scanning a sphere, on the left a video using the front view and on the right the top view. 

<img src="https://github.com/jonathashmp/HAG_Topology/blob/main/Videos/H-A%20Gripper%201.gif" width=40% height=40% /> <img src="https://github.com/jonathashmp/HAG_Topology/blob/main/Videos/H-A%20Gripper%202.gif" width=50% height=50% />

## Instructions

These instructions aim to explain the results found in this work and which are attached in the experiment results folder.

With this shared data, it is possible to reconstruct the analysis of each experiment.

### 1 - H-A Grippers design and experiments.

This claw is a project developed with affordable electronic devices and structural parts printed in PLA using 3D printers. The H-A gripper uses seventeen VL53L0X sensors to detect and scan the objects, nine MG996R servo motors to control all grip movements and an Arduino MEGA microcontroller to work with.

All experiments were processed on Ubuntu 18.04 with ROS Melodic 1.14.13 and MATLAB R2022a. ROS was used to integrate Arduino with MATLAB.

All objects used in the experiments were printed from 3D printers and can be found in the [STL files](https://github.com/jonathashmp/Non-Contact-Tactile-Perception-for-Hybrid-Active-Gripper/tree/main/STL%20files).

Steps used to perform the experiments:

1 - Connecting the arduino with rosserial and MATLAB.

2 - Place the object in front of the palm of the gripper and start the simulation.

3 - Waiting for the process and at the end a file with the results will be created.

4 - These results are used in predicting objects.

You can [watch video](https://github.com/jonathashmp/Non-Contact-Tactile-Perception-for-Hybrid-Active-Gripper/blob/main/Videos/project%20scan%20simulation.mp4) to better understand this stage of experiments

### 2 - Analyzing the results in Matlab.

The results were separated at two parts. A folder with the individual results of each experiment realized and other folder with the all results together of each object.

1 - [Folder with the individual results of each simulation of each object](https://github.com/jonathashmp/Non-Contact-Tactile-Perception-for-Hybrid-Active-Gripper/tree/main/Results%20of%20experiments/individual%20files%20of%20each%20simulation%20by%20object).

This instruction is to show how the files were stored and processed in Matlab. You can use this information and make your analysis with the results     obtained in this project. 

There are eleven folders in this directory, where each folder contains the results collected in each experiment performed for each object.

The name of the files is using the following structure:

**object_simulation_closing_step**

Object is the name of the scanned object. Example: bottle, cube_40, etc.

The simulation is the identification of which experiment was performed, ranging from 1 to 5, because for each object five repetitions of experiments were performed.

Closing is the angle of closure of the finger at the time of data collection. This variation can be 60º, 70º, 80º or 90º which were the angles at which the fingers were positioned to collect the data.

Step is the number of variations performed by the gripper while reading the data. Power 6 for variation from 0º to 180º from 30 to 30 degrees, 9 for variations from 0º to 180º from 20 to 20 degrees and 18 for variations from 0º to 180º from 10 to 10 degrees.

These data were processed in matlab software with the dalaunay triangulation function to make the object prediction. With this function it was possible to compare the scanned object with the object file that was printed on the 3D printer that is in the [STL files](https://github.com/jonathashmp/Non-Contact-Tactile-Perception-for-Hybrid-Active-Gripper/tree/main/STL%20files).

2 - [Folder with the results of each object in a single file](https://github.com/jonathashmp/Non-Contact-Tactile-Perception-for-Hybrid-Active-Gripper/tree/main/Results%20of%20experiments/files%20of%20all%20simulations%20by%20object).

In this instruction you can do an analysis of each object with all experiments in a single file.

In this folder you will find the files saved with the names of the objects and all the data in csv format. With these data it is possible to make a global analysis of the experiments.
