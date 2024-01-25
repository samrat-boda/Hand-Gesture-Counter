
# Hand-Gesture-Counter


A brief description of what this project does and who it's for

This project focuses on hand gesture recognition using a webcam. The program captures video, identifies the hand in the frame, and analyzes its features to determine the number of fingers being held up. The process involves initializing video capture, defining a region of interest (ROI), calculating extreme points, estimating the hand center, creating a circular region, and identifying extended fingers. Additionally, the program employs background calculation for the first 60 frames to enhance hand segmentation.

# Usage
## 1)Initialize Video Capture:

The program begins by initializing a connection to the webcam using OpenCV's cv2.VideoCapture(0).
## 2)Define Region of Interest (ROI):

A specific area in each frame, known as the Region of Interest (ROI), is defined. This is where the program expects the hand to appear.
## 3)Calculate Extreme Points:

Identify the most outward points in the hand's contour using cv2.convexHull.

![image](https://github.com/samrat-boda/Hand-Gesture-Counter/assets/88550792/09569cca-650d-40eb-b0c5-d51384c96a62)


## 4)Estimate Hand Center:

Find the center of the hand by calculating the intersection of the extreme points.
## 5)Calculate Maximum Distance:

Determine the maximum distance between the hand center and the most external points on the convex hull.
## 6)Create Circular Region:

Create a circle around the estimated hand center with a radius based on a certain ratio of the maximum distance.
## 7)Identify Extended Fingers:

Points outside the created circle and significantly above the bottom of the hand are considered as extended fingers, indicating the number of fingers being held up.
## 8)Background Calculation (First 60 Frames):

For the initial 60 frames, the program calculates the average background using cv2.accumulateWeighted. This helps distinguish the hand from the background.
## 9)Hand Segmentation and Visualization:

After background subtraction, the program identifies and draws contours around the segmented hand, displays the finger count, and shows a binary thresholded image for visualizing hand features, all within the specified ROI. This involves using cv2.absdiff, cv2.threshold, and cv2.findContours.
![image](https://github.com/samrat-boda/Hand-Gesture-Counter/assets/88550792/bece9c57-d2ff-48b2-86cf-32ec100e885e)


## Setup and Requirements

OpenCV: Ensure you have OpenCV installed. You can install it using:

 
# Setup and Requirements

## OpenCV Installation
Ensure you have OpenCV installed. You can install it using:

```bash
pip install opencv-python

 
