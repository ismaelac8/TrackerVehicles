# Vehicle Detection in Traffic Videos Using Deep Learning

This project focuses on detecting vehicles and estimating their speeds in traffic videos using deep learning techniques. By leveraging the YOLOv5 algorithm and tools such as the CARLA simulator, both real and simulated scenarios are used to evaluate the performance of the system.

![Project Demo](./images/demo.png)

## Project Overview

The primary objective of this project is to develop a system capable of identifying vehicles in traffic videos and estimating their relative speeds to the camera. The YOLOv5 object detection algorithm is used alongside trajectory tracking and speed estimation techniques.

## Contents

- `Memoria_TFG_Ismael_Aguilera.pdf`: Complete documentation of the Final Degree Project, detailing objectives, development, and results.
- `Ism-ultralytics_yolov5.ipynb`: Jupyter Notebook containing the implementation code for YOLOv5 to detect vehicles.
- `demovideoreal.mp4`: Demo video showcasing the system in action.

## Requirements

To run this project, you will need:

- Python 3.8 or higher
- Python libraries: `torch`, `opencv-python`, `norfair`, `ultralytics`
- CARLA Simulator (optional for generating simulated traffic videos)
- Google Colab (optional for running the notebook)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your_username/your_project.git
    cd your_project
    ```

2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download YOLOv5 weights:
    ```bash
    wget https://github.com/ultralytics/yolov5/releases/download/v6.0/yolov5s.pt -P models/
    ```

## Usage

### Running the Notebook

1. Open `Ism-ultralytics_yolov5.ipynb` in Jupyter or Google Colab.
2. Execute all the cells to load the data, train the model (if necessary), and perform vehicle detection on traffic videos.

### Generating Videos with CARLA

1. Install and configure CARLA by following the official instructions at [CARLA Simulator](https://carla.org/).
2. Use the scenario generation scripts to create simulated videos with various vehicle behaviors.
3. Process the generated videos using the notebook for detection and speed estimation.

## Detailed Explanation

### YOLOv5 for Vehicle Detection

YOLOv5 (You Only Look Once) is a state-of-the-art object detection algorithm known for its speed and accuracy. This project uses a pre-trained YOLOv5 model fine-tuned on traffic videos to detect vehicles. The model takes video frames as input and outputs bounding boxes around detected vehicles.

### Speed Estimation

Once vehicles are detected, their trajectories are tracked across frames to estimate their speeds. The project employs optical flow and other tracking techniques to ensure accurate speed calculations relative to the camera.

### Simulated vs. Real Scenarios

The project uses both real-world traffic videos and simulated scenarios generated using the CARLA simulator. This approach allows for comprehensive evaluation and ensures that the system performs well under various conditions.

## Results

![Detection Results](./images/results.png)

The system has been evaluated on both real and simulated videos, demonstrating high accuracy in vehicle detection and reliable speed estimation. Detailed results and analysis can be found in `Memoria_TFG_Ismael_Aguilera.pdf`.

## Contributions

Contributions are welcome. If you wish to collaborate, please fork the repository and submit a pull request with your improvements.

## Contact

For any inquiries or suggestions, you can reach me at: ismaelaguileracevera8@gmail.com

---

This README provides a comprehensive overview of the project, including installation instructions, usage details, and explanations of the methodologies used. You can further customize it with more specific information or images as needed.
