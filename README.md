# Smart Traffic Light Control System using YOLO

This project implements an **AI-powered smart traffic light system** that dynamically controls signal timings using **real-time vehicle detection**. It eliminates unnecessary red light wait times by detecting traffic presence using the **YOLO object detection algorithm**.

---

# Objective

To reduce traffic congestion and improve fuel efficiency by:
- Automatically extending green signals when traffic is detected.
- Skipping unnecessary red lights when no traffic is present.

---

# Key Features

- **YOLO-based vehicle detection** (cars, bikes, buses, trucks, etc.)
- Real-time decision logic for traffic light control
- Optimized green/red light durations based on detected traffic
- No traffic = no red signal delay
- Works with live video or pre-recorded footage

---

# Tech Stack

- **Python 3.x**
- **OpenCV** – For video capture and frame processing
- **YOLOv4 / YOLOv5** – For object detection
- **NumPy** – Array operations
---

# Project Structure
smart-traffic-light/
│
├── yolo-cfg/ # YOLO model config and weights
│ ├── yolov4.cfg
│ ├── yolov4.weights
│ └── coco.names
│
├── traffic_control.py # Main logic for vehicle detection and signal control
├── utils.py # Helper functions for drawing, counting, etc.
├── input/ # Sample video or live camera input
│ └── traffic.mp4
│
└── output/ # Processed video with overlays
└── traffic_output.mp4

![image](https://github.com/user-attachments/assets/978d87eb-4d86-450c-a6de-78912b7c9dd8)


---

# How It Works

1. Load YOLO model with pre-trained weights
2. Read frames from video or live webcam
3. Detect objects (vehicles) in each frame
4. Count number of vehicles per lane
5. If vehicle count exceeds a threshold:
       -> Extend green signal
   Else:
       -> Skip red and switch to next lane
6. Display updated signal status and bounding boxes
7. Repeat...

# Dataset Used
YOLO pre-trained on COCO dataset
Detects: car, bus, truck, motorcycle, bicycle, etc.

# Future Improvements
Integrate with Raspberry Pi or Arduino for real-world deployment
Add emergency vehicle detection
Use license plate recognition (ALPR) for rule enforcement
Log traffic density data for smart city analytics

---

# Authors

*1. Jayesh Gawde*

*2. Shrutee Salpe* 

*3. Parth Gupta* 

---
