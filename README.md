This repository contains the code and report for 25COC001 Robotics.

It uses a lightweight **MobileNet-V3 Small** neural network to look at the track, predict the line's center point, and steer the robot in real-time.

---

## Contents

### Training and Inference
* **`regression_inference.ipynb`**: The main control loop that runs live on the robot.
* **`regression_algorithm.ipynb`**: The training pipeline.
* **`motors.py`**: Provided helper class to control robot.

### Data Collection & Processing
* **`video_capture.ipynb`**: Captures raw camera feeds during manual driving runs to build the training dataset.
* **`video_processing_regression`**: Notebook to process and label dataset.

---

## How to Run

### 1. Train the Model
To train the enhanced steering model using the images in `regression_dataset/` using **`regression_algorithm.ipynb`**.

The best model checkpoint will be saved directly in the `models/` folder.

### 2. Deploy on the Robot
To start the live control loop on the physical robot, run **`regression_algorithm.ipynb`**.