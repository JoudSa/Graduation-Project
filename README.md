# Graduation-Project
A real-time driver drowsiness detection system utilizing YOLOv11n
# Culturally Robust Driver Drowsiness Detection

This repository contains the real-time detection script and fine-tuned YOLOv11n model weights for a culturally adaptive driver-monitoring system. 

The system bypasses the limitations of traditional full-face landmark algorithms by treating the eye region as an isolated object, allowing it to accurately detect drowsiness even when the driver's lower face is covered by cultural attire such as a niqab, hijab, or shemagh.

## Files
* `live_stream.py`: The main execution script utilizing OpenCV for frame capture, YOLO11n for inference, and Pygame for procedural audio alerts (880Hz warning and 1200Hz critical alarm).
* `best.pt`: The YOLOv11 Nano weights, trained for 100 epochs on a custom hybrid dataset of 5,000 images (achieving mAP@0.5 of 0.9877).

## Requirements
* Python 3.x
* OpenCV (`cv2`)
* Ultralytics YOLO (`ultralytics`)
* Pygame
* NumPy

## Usage
Run the main script to start the webcam feed and initiate real-time drowsiness monitoring:
`python live_stream.py`
