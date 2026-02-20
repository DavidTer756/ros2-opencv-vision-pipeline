This repository contains a modular computer vision system developed as part of the TRSA (Robotics and Industrial Automation) curriculum at NOVA SST. The project focuses on building a robust camera-to-processing pipeline using ROS 2 Humble and OpenCV to perform real-time sensing, calibration, and object detection.

### Key Implementation Features:
- **Camera Driver Node:** Interfaces with hardware using OpenCV's VideoCapture to stream live frames over the ROS network under the `/camera/image_raw` topic.
- **ROS-OpenCV Bridge:** Implemented `cv_bridge` for seamless conversion between `sensor_msgs/Image` and `cv::Mat` formats, ensuring high-performance real-time processing.
- **Distortion Rectification:** Performed full camera calibration using a chessboard pattern to generate a calibration matrix (YAML), rectifying radial distortion for accurate spatial measurements.
- **Image Processing Pipeline:** Developed nodes for grayscale conversion, Gaussian blurring ($21 \times 21$ kernel), and Canny Edge Detection to extract environmental features.
- **Autonomous Object Detection:** Created an `object_detection` node using traditional computer vision techniques to identify and track specific items via bounding boxes in a live stream.
