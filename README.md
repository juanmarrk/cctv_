# CCTV Surveillance Analysis Project

# Collaborators :
                 - Sparsh Anand
                 - Juan Mark Deen
                 - Vaastav Upadhyaya
                 - Priyanshi Jaiswal

## Overview

Welcome to the CCTV Surveillance Analysis project! This project is designed to help you analyze and process video footage from CCTV cameras for various purposes, including security monitoring, object detection, and more. This README file provides an overview of the project, its features, and how to get started.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Features

This project offers a range of features to assist in CCTV surveillance analysis:

1. **Video Streaming**: Capture live video feed from CCTV cameras or process pre-recorded video files.

2. **Object Detection with YOLO**: Utilize YOLO (You Only Look Once) for efficient and accurate object detection.
   - YOLO divides the image into a grid and predicts bounding boxes and class probabilities for objects within each grid cell.
   - YOLO operates in a single forward pass of a neural network, making it very fast.

3. **Object Tracking with DeepSort (Deep SORT)**: Implement object tracking with DeepSort.
   - DeepSort combines deep learning with tracking techniques to associate and track objects across video frames.
   - It assigns unique IDs to objects and maintains their tracks over time.

4. **Alerts and Notifications**: Trigger alerts and notifications when specific events or objects are detected.

5. **Motion Detection**: Implement motion detection algorithms to identify and flag suspicious activities.

6. **Data Storage**: Save video footage and analysis results for later review and archiving.

7. **Web Interface**: Access the system through a user-friendly web interface for monitoring and configuration.

8. **API Integration**: Integrate the analysis results with other systems or services via APIs.

9. **OpenCV (Open Source Computer Vision Library)**: Leverage OpenCV for a wide range of image and video processing tasks.
   - OpenCV is used for drawing bounding boxes around detected and tracked objects, line drawing, text annotations, and various image processing operations.

10. **Euclidean Distance**: Calculate Euclidean distance to estimate the speed of objects based on their position changes between frames.
    - Euclidean distance is used in conjunction with known pixels-per-meter (ppm) ratios to calculate speed in kilometers per hour (km/h).

11. **Non-Maximum Suppression (NMS)**: Apply NMS to YOLO detection results to filter out overlapping and less confident bounding boxes.

12. **Bounding Box Transformation**: Convert bounding box coordinates between formats using functions like `xyxy_to_xywh` and `xyxy_to_tlwh` for consistency and compatibility.

13. **Color Encoding**: Assign unique colors to different object classes using the `compute_color_for_labels` function for visualization purposes.

14. **Direction Calculation**: Calculate the direction of object movement (e.g., North, South, East, West) based on their position changes between frames.

15. **Object Tracking**: Maintain the identity of objects across multiple frames of a video using DeepSort, which assigns unique IDs to tracked objects and predicts their positions in subsequent frames.

16. **Speed Estimation**: Estimate the speed of objects based on the change in their positions between frames using the `estimatespeed` function.

17. **Drawing and Visualization**: Use OpenCV functions for drawing bounding boxes around objects, line drawing for visualizing motion paths, and text annotations.

18. **Hydra Configuration**: Utilize Hydra configuration management to separate configuration parameters from the code, allowing for easy customization of settings without modifying the code directly.

## Requirements

To use this project, you'll need the following:

- **Hardware**:
  - CCTV cameras or video input sources.
  - Sufficient processing power and memory for video analysis (requirements may vary based on the complexity of analysis).

- **Software**:
  - Operating System (e.g., Linux, Windows, macOS).
  - Python 3.x with required packages (see [Installation](#installation)).
  - Web server software (e.g., Apache, Nginx) for the web interface (optional).

## Installation

Follow these steps to set up the CCTV Surveillance Analysis project:

1. Clone the project repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/CCTV-Surveillance-Analysis.git
   cd cctv-surveillance-analysis
   ```

2. Create a virtual environment (recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Configure the project settings, including camera configurations, object detection models, and alert settings.

5. Start the analysis system:

   ```bash
   python main.py
   ```

6. Access the web interface by opening a web browser and navigating to `http://localhost:8080` (adjust the port as needed).

## Usage

1. **Adding Cameras**: Configure the system to connect to your CCTV cameras or video sources. Make sure to provide the necessary credentials and settings.

2. **Object Detection**: Define the objects you want to detect and track within the video feed. You can use pre-trained YOLO models for this purpose.

3. **Alerts and Notifications**: Set up alerting mechanisms, such as sending emails or text messages when specific events occur (e.g., unauthorized access, object detection).

4. **Monitoring**: Use the web interface to monitor the live video feed, review recorded footage, and access analysis results.

5. **Data Management**: Manage storage and archiving of video footage and analysis data to ensure efficient use of resources.

## Contributing

Contributions to this project are welcome! If you have ideas for improvements, bug fixes, or new features, please feel free to open an issue or submit a pull request on the project's GitHub repository.
---

Thank you for using the CCTV Surveillance Analysis project. If you have any questions or need assistance, please don't hesitate to reach out to the project maintainers or the community. Happy analyzing!
