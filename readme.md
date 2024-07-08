**Image Registration using ORB and Homography**

**Overview**
This Python script performs image registration using the Oriented FAST and Rotated BRIEF (ORB) feature detector and descriptor, along with homography estimation. Image registration is the process of aligning two images to find a spatial transformation that best aligns corresponding features in the images.

**Requirements**
Python 3.x
OpenCV (cv2)
NumPy

Steps: 

(1) Download the script file.
(2) Place the script file and your input images in the same directory.
(3) Run the script using a Python interpreter or google colab 

You can use this script to run the code file: 
                           python image_registration.py
(4) The script will perform image registration using ORB feature detection and homography estimation. The aligned image will be saved as output.jpg in the same directory.

**Description**

(1) The script first reads two input images (Example1_fixed.tif and Example1_moving.tif) that you want to align.

(2) It converts the images to grayscale and detects keypoints and computes descriptors using the ORB feature detector.

(3) Matches between the keypoints in the two images are found using a Brute Force matcher with Hamming distance as the measurement mode.

(4) The matches are sorted based on their Hamming distance, and the top 90% of matches are retained.

(5) The script then estimates the homography matrix using the RANSAC algorithm based on the matched keypoints.

(6) Finally, the script warps the first image (Example1_fixed.jpg) according to the estimated homography matrix and saves the aligned image as output.jpg.