# Density Based Smart Traffic Control System Using Canny Edge Detection Algorithm

This project implements a traffic control system based on density detection using the Canny Edge Detection algorithm. The system processes traffic images to detect vehicle density and dynamically allocates green signal time based on the detected traffic density.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [How It Works](#how-it-works)
- [Future Enhancements](#future-enhancements)
- [License](#license)

## Overview
The system uses the Canny Edge Detection algorithm to process traffic images and determine the density of vehicles. The algorithm involves several steps including image smoothing, gradient calculation, non-maximum suppression, double thresholding, and edge tracking by hysteresis. The processed image is then analyzed to count the number of white pixels, which represent the detected edges (vehicles).

## Features
- Upload traffic images for processing
- Apply Canny Edge Detection to detect vehicle edges
- Count the number of white pixels (edges) in the processed image
- Calculate and display green signal allocation time based on detected traffic density

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/traffic-control-canny-edge.git
    cd traffic-control-canny-edge
    ```
2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Run the main application:
    ```bash
    python main.py
    ```
2. Upload a traffic image by clicking the "Upload Traffic Image" button.
3. Preprocess the image using the "Image Preprocessing Using Canny Edge Detection" button.
4. Count the white pixels in the processed image using the "White Pixel Count" button.
5. Calculate and display the green signal time allocation based on traffic density using the "Calculate Green Signal Time Allocation" button.

## Project Structure
traffic-control-canny-edge/
│
├── images/ # Folder containing sample traffic images
├── gray/ # Folder containing processed images
├── main.py # Main application script
├── CannyEdgeDetector.py # Canny Edge Detection algorithm implementation
├── README.md # Project README file
├── requirements.txt # List of dependencies
└── utils.py # Utility functions (if any)


## Dependencies
- Python 3.x
- NumPy
- SciPy
- OpenCV
- Matplotlib
- scikit-image
- Tkinter

## How It Works
1. **Gaussian Smoothing:** Smooth the image using a Gaussian filter to reduce noise.
2. **Gradient Calculation:** Use Sobel filters to calculate the gradient magnitude and direction.
3. **Non-Maximum Suppression:** Thin the edges to create a binary edge image.
4. **Double Thresholding:** Apply a high and low threshold to classify strong, weak, and non-relevant edges.
5. **Edge Tracking by Hysteresis:** Finalize the edge detection by suppressing all weak edges that are not connected to strong edges.
6. **Pixel Count:** Count the number of white pixels in the processed image to estimate vehicle density.
7. **Time Allocation:** Calculate green signal time based on the ratio of detected vehicle density to reference density.

## Future Enhancements
- Integrate real-time video feed processing for dynamic traffic control.
- Enhance the algorithm to differentiate between various types of vehicles.
- Develop a web-based interface for remote monitoring and control.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to contribute to this project by submitting issues or pull requests.
