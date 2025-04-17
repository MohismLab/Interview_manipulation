# Interview_manipulation

## Project Overview

This project is designed to evaluate students' understanding of robotic grasping systems, the application of deep learning models, and the integration of simulation environments. The task is based on the `manipulator_grasp` project, which uses the GraspNet model to detect grasp poses from point cloud data and controls a UR5 robotic arm in the Mujoco simulation environment to execute grasping operations.

### Objectives:
1. Successfully reproduce the basic grasping functionality of the project (as shown in `demo_1.mp4`).
2. Extend the project to implement sequential grasping and placement of **all** graspable objects in the scene.

---

## Prerequisites

- **Operating System**: Ubuntu 22.04
- **GPU**: NVIDIA GPU with CUDA support
- **Environment Management**: Conda
- **Python Version**: 3.10

---

## Installation Guide

### 1. Environment Setup

1. **Clone the Repository**:
   ```bash
   git clone --recurse-submodules -j8 https://github.com/MohismLab/Interview_manipulation.git
   cd manipulator_grasp
   ```

2. **Download GraspNet Model**:
   Follow the instructions in the [GraspNet Baseline repository](https://github.com/graspnet/graspnet-baseline) to download the pre-trained model. Place the model files in the `graspnet-baseline` directory.

3. **Create and Activate Conda Environment**:
   ```bash
   conda create -n your_env_name python=3.10
   conda activate your_env_name
   ```

4. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

---

## Task Instructions

### 1. Basic Functionality: Single Object Grasping

- **Goal**: Reproduce the basic functionality of the project, as demonstrated in `demo_1.mp4`.
- **Steps**:
  1. Run the main program:
     ```bash
     python main.py
     ```
  2. Observe the Mujoco simulation window. The UR5 robotic arm should:
     - Detect the best grasp point for a single object.
     - Move to the grasp point.
     - Grasp the object.
     - Lift the object and optionally place it in a predefined location.

- **Expected Outcome**: The robotic arm successfully completes the grasping operation for a single object.

---

### 2. Advanced Functionality: Grasping All Objects in the Scene

- **Goal**: Modify the code to enable the robotic arm to:
  - Detect and grasp **multiple objects** in the scene.
  - Sequentially grasp each object and place it in a designated area.

---

## Submission Guidelines

### 1. Code Submission

- Provide a **private GitHub repository** containing all the code used for this task.
- Add **QingbiaoLI** (`qingbiao.qli@gmail.com`) as a collaborator to your repository.
- Ensure the repository includes a clear `README.md` file with instructions on how to:
  - Run your code.
  - Reproduce both the basic and advanced functionalities.

### 2. Reporting

- Prepare a concise report (2-3 pages) addressing the following:
  1. **Basic Functionality**:
     - How did you reproduce the basic functionality?
     - What challenges did you encounter, and how did you resolve them?
  2. **Advanced Functionality**:
     - How did you design and implement the sequential grasping functionality?
     - Provide a detailed explanation of your algorithm and key code modifications.
  3. **Results**:
     - Include screenshots or video links demonstrating the advanced functionality.
  4. **Challenges and Improvements**:
     - Discuss any challenges faced during the implementation.
     - Suggest potential improvements or further extensions to the project.

- **Recommendation**: Use LaTeX (via Overleaf) to write the report for better formatting.

---
