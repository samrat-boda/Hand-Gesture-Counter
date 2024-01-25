Project Name Readme
Project Overview
This project focuses on hand gesture recognition using a webcam. The program captures video, identifies the hand in the frame, and analyzes its features to determine the number of fingers being held up. The process involves initializing video capture, defining a region of interest (ROI), calculating extreme points, estimating the hand center, creating a circular region, and identifying extended fingers. Additionally, the program employs background calculation for the first 60 frames to enhance hand segmentation.

```bash
# Setup and Requirements

## OpenCV Installation
Ensure you have OpenCV installed. You can install it using:

```bash
pip install opencv-python
