# Car Counting Project

This project implements a vehicle counting system using the YOLOv10 model for object detection and the SORT algorithm for tracking. The system counts vehicles crossing a designated line in a video feed.

## Features
- **Object Detection:** Utilizes YOLOv10 for detecting various classes of objects including cars, trucks, buses, and motorbikes.
- **Object Tracking:** Implements the SORT (Simple Online and Realtime Tracking) algorithm for tracking objects across frames.
- **Custom Masking:** Applies a mask to focus the detection on a specific region of interest in the video feed.
- **Counting Logic:** Counts vehicles that cross a defined line within the frame, using their center coordinates.

## How It Works
1. **Object Detection:**
   - The script uses a pre-trained YOLOv10 model (`yolov10l.pt`) to detect objects in each frame of the video.
   - Classes detected include `person`, `bicycle`, `car`, `motorbike`, `aeroplane`, `bus`, `train`, `truck`, etc.
   - Only vehicles (`car`, `truck`, `bus`, `motorbike`) with confidence scores above 0.3 are considered for counting.

2. **Tracking:**
   - The SORT tracker is used to maintain the identity of vehicles across frames, allowing for accurate counting.
   - Each vehicle is assigned an ID that persists until it leaves the frame.

3. **Counting:**
   - A red line is drawn at a specific position in the frame, acting as the counting threshold.
   - Vehicles crossing this line are counted, and the count is displayed on the frame.
   - The line changes color to green when a vehicle is successfully counted.

## Prerequisites
- Python 3.x
- OpenCV
- YOLOv10 (from `ultralytics` package)
- `cvzone` library for drawing bounding boxes and text.
- `sort` library for tracking.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/proxi666/car-counting.git

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
3. Ensure you have the necessary YOLOv10 weights (yolov10l.pt) in the root directory.

## Usage
1. Place the input video file (e.g., cars.mp4) in the project directory.
2. Run the car_counter.py script:
   ```bash
   python car_counter.py
3. The script will display the video feed with detected and tracked vehicles, along with the count of vehicles that have crossed the line.



   
