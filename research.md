# Research

## Overview
This research explores the transition from classical robotics to **end-to-end learning-based methods** for robotic manipulation. The goal is to create adaptable, cost-effective systems capable of handling dynamic real-world scenarios.

---

## Classical Robotics: Pick-and-Place Pipeline
- **Framework**: Built using the Drake robotics framework with a KUKA iiwa robot.
- **Key Features**:
  - Defined spatial transformations and trajectories for pick-and-place tasks.
  - Achieved high precision using pseudoinverse-based inverse kinematics.
- **Limitations**:
  - Sensitivity to object variations.
  - Lack of adaptability in dynamic environments.
  - Challenges with kinematic singularities.

> **Demo Video**: [Pick-and-Place Pipeline in Action](https://drive.google.com/drive/u/0/folders/1LftoRg34HieBMN42KgWSghgstuSexj5M)

---

## Learning-Based Approaches: ACT and Diffusion Policies
### 1. Action Chunking with Transformers (ACT)
- **Focus**: Predicting temporally coherent action sequences to minimize errors.
- **Techniques**:
  - **Action Chunking**: Groups actions to ensure smooth execution.
  - **Temporal Ensembling**: Mitigates abrupt transitions.
- **Applications**:
  - Pick-and-place tasks.
  - Object sliding.
- **Key Advantage**: Superior motion fluidity.

> **Demo Post**: [ACT in Action](https://www.linkedin.com/feed/update/urn:li:activity:7279526421532708864/)  

---

### 2. Diffusion Policies
- **Focus**: High-precision trajectory refinement through iterative denoising.
- **Techniques**:
  - Models trajectory distributions in action space.
  - Iteratively adjusts actions to account for variations.
- **Applications**:
  - Object stacking.
  - Complex rotations and orientation tasks.
- **Key Advantage**: Handles dynamic changes effectively.

> **Demo Post**: [Diffusion Policies in Action](https://www.linkedin.com/feed/update/urn:li:activity:7279526421532708864/) 

---

## Experimental Results
### Success Rates for Tasks

- **Pick-and-Place**:  
  - ACT Success Rate: 83%  
  - Diffusion Policies Success Rate: 85%  

- **Object Sliding**:  
  - ACT Success Rate: 65%  
  - Diffusion Policies Success Rate: 72%  

- **Object Stacking**:  
  - ACT Success Rate: 78%  
  - Diffusion Policies Success Rate: 82%  

- **Object Orientation**:  
  - ACT Success Rate: 75%  
  - Diffusion Policies Success Rate: 83%  

> **Insights**:
> - **ACT**: Best for smooth and consistent task execution.
> - **Diffusion Policies**: Excels in precision-heavy tasks.

---

## Hardware Setup
### Leader-Follower Robotic Arm System
- **Leader Arm**: Controlled by a human operator for task demonstration.
- **Follower Arm**: Mimics the leader's movements to collect high-quality training data.
- **Features**:
  - 6-DoF robotic manipulators with Dynamixel servos.
  - Cost-effective and scalable for smaller labs.
- **Vision System**:
  - Dual RGB cameras for workspace coverage.
  - High-resolution and consistent field-of-view.

> **Image**:  
![Hardware Setup](images/r2.jpg)

---

## Explore More
### Videos and Resources
- [Results and Details](https://drive.google.com/drive/u/0/folders/1LftoRg34HieBMN42KgWSghgstuSexj5M)
- [Thesis](https://drive.google.com/file/d/1C7pAfuXQWmzh2rpmZ7TqhSQl00mkbWvf/view?usp=drive_link)

---

## References
For additional technical details and algorithms, refer to my [Master’s Thesis](https://drive.google.com/drive/u/0/folders/1LftoRg34HieBMN42KgWSghgstuSexj5M).