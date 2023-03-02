# Hybrid-Active-Gripper-A-Novel-Topology-for-Object-Grasping

This study presents a novel topology of a robotic gripper with three reconfigurable fingers. Each finger can move 180º around the object and adjust its lateral inclination by up to 10º to obtain the best configuration to pick up an object. The gripper has two models designed and printed on a 3D printer using plastic polymer (PLA) material. These models have 12 degrees of freedom (DoF) each, the main difference between them being the finger closure, as the Hybrid-Active (H-A) gripper 1 uses the closure of the distal phalanx through a link with the middle phalanx and the H-A gripper 2 has independent control of each degree of freedom.

Below we have the two versions of the claw with its exploded view. On the left side is the H-A Gripper one that has finger closure control through a link, and on the right side, we have the H-A Gripper two that uses micro servos to control the phalanges.

<img src="https://github.com/jonathashmp/HAG_Topology/blob/main/Videos/H-A%20Gripper%201.gif" width=50% height=50% /> <img src="https://github.com/jonathashmp/HAG_Topology/blob/main/Videos/H-A%20Gripper%202.gif" width=50% height=50% />

## 1 - Instructions

These instructions explain how H-A grippers work and the parts needed to rebuild the gripper using a 3D printer. 

With this information, you can assemble the grips by downloading the [STL files of the H-A gripper one and two](https://github.com/jonathashmp/HAG_Topology/tree/main/STL%20H-A%20Grippers%201%20and%202).

### 1.1 - Mechanism of Fingers Closing

The finger close mechanism is responsible for gripping the object and its structure can be seen in figure below. The figure shows two types of fingers: the left finger is from H-A gripper one, and the right finger is from H-A gripper two.

<img src=https://github.com/jonathashmp/HAG_Topology/blob/main/Figures/3D%20exploded%20view%20of%20finger%20closing%20mechanism.png />

In this figure, it is possible to observe the step-by-step assembly of the two types of fingers. All these parts can be printed using the files in the [STL H-A Grippers 1 and 2 folder](https://github.com/jonathashmp/HAG_Topology/tree/main/STL%20H-A%20Grippers%201%20and%202).

### 1.2 - Finger Tilt Adjustment

The finger tilt control allows a variation of up to 10º of lateral inclination for each finger to help adjust the gripper to obtain the ideal position to perform the pick-up and its structure can be seen in figure below. The figure shows only a structure to finger tilt adjustment because the H-A gripper one and two have the same design.

<img src=https://github.com/jonathashmp/HAG_Topology/blob/main/Figures/3D%20view%20of%20the%20Finger%20Tilt%20Adjustment.png />

In this figure, it is possible to observe the step-by-step assembly of the two types of fingers. All these parts can be printed using the files in the [STL H-A Grippers 1 and 2 folder](https://github.com/jonathashmp/HAG_Topology/tree/main/STL%20H-A%20Grippers%201%20and%202).

### 1.3 - Angular Arrangement of Fingers

The H-A gripper was the ability to rotate fingers around the object about the ''palm'' of the gripper. With this control, each finger can vary its position from 0º to 180º to find the ideal position to perform the pick-up. In figure below, we have an exploded view of the 3D project of this gripper control that will help us better understand how this rotational movement of the fingers occurs.
