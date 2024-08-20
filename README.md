Car Counting Project
This project implements a vehicle counting system using the YOLOv10 model for object detection and SORT algorithm for tracking. The system counts vehicles crossing a designated line in a video feed.

Features:
Object Detection: Utilizes YOLOv10 for detecting various classes of objects including cars, trucks, buses, and motorbikes.
Object Tracking: Implements the SORT (Simple Online and Realtime Tracking) algorithm for tracking objects across frames.
Custom Masking: Applies a mask to focus the detection on a specific region of interest in the video feed.
Counting Logic: Counts vehicles that cross a defined line within the frame, using their center coordinates.
