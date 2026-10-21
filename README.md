# Unmanned Shop

AI-powered unmanned shop system that detects people, assigns IDs, and tracks movement using multi-camera calibration.

## Overview

This project implements a multi-camera calibration and tracking pipeline for an unmanned shop environment. The goal is to accurately detect people across multiple camera views, assign consistent identities, and track their movement in a shared 3D space using synchronized camera data.

## Key Features

- Multi-camera calibration for spatial alignment
- Person detection across camera viewpoints
- Identity assignment and tracking across frames
- 3D pose and movement analysis
- Real-time monitoring for retail or surveillance applications
- Python-based implementation using OpenCV and MediaPipe

## Technologies

Python, OpenCV, MediaPipe, Multi-camera calibration, Real-time body detection

## Repository Structure

```text
Multi_Camera_Calibration/
├── data/
│   ├── extrinsics/
│   ├── frames/
│   ├── intrinsics/
│   ├── mediapipe/
│   └── selected/
├── results/
│   ├── extrinsic_params.npy
│   ├── intrinsic_params.npy
│   └── joint_optimized_params.npy
├── src/
│   ├── calibration/
│   ├── capture/
│   ├── data_selection/
│   ├── pose_detection/
│   ├── visualization/
│   ├── main.py
│   ├── triangulate_3d.py
│   └── visualize_3d.py
├── environment.yml
├── requirements.txt
├── fixed_joints.py
├── run_3d_pose.py
├── README.md
├── .gitignore
└── ...
```

## Setup

### Requirements

- Python 3.x
- OpenCV
- NumPy
- MediaPipe
- Matplotlib

### Install dependencies

```bash
pip install -r requirements.txt
```

or with Conda:

```bash
conda env create -f environment.yml
conda activate <environment_name>
```

## Usage

Run the main 3D pose pipeline:

```bash
python run_3d_pose.py
```

The project loads calibration data and pose information to reconstruct 3D movement in a common coordinate system.

## Use Case

This system is suited for:

- unmanned retail stores
- smart surveillance
- activity monitoring
- person tracking in multi-camera environments

## Notes

This repository is focused on multi-camera calibration and human tracking in a shared coordinate frame, enabling real-world monitoring and analysis in complex indoor spaces.
