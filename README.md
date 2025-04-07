# Facial Recognition Attendance System

A modern attendance tracking system that uses facial recognition technology to automatically mark attendance by detecting and identifying faces through a webcam feed.

## Features

- Real-time face detection and recognition
- Automatic attendance marking
- CSV export of attendance records
- Support for multiple face encodings
- Easy to use interface

## Prerequisites

Before you begin, ensure you have the following installed:
- Python 3.11 or higher
- OpenCV
- face_recognition library
- dlib
- numpy

## Installation

1. Clone this repository or download the source code
2. Install the required dependencies:
   ```bash
   pip install opencv-python
   pip install face-recognition
   pip install numpy
   ```
3. Install dlib using the provided wheel file:
   ```bash
   pip install dlib-19.24.1-cp311-cp311-win_amd64.whl
   ```

## Project Structure

```
├── ImagesAttendance/     # Directory containing reference face images
├── attendance.csv        # CSV file storing attendance records
├── attendanceProject.py  # Main application script
└── README.md            # Project documentation
```

## Usage

1. Add reference images:
   - Place clear face images of individuals in the `ImagesAttendance` folder
   - Name the images as per the person's name (e.g., "John Doe.jpg")

2. Run the application:
   ```bash
   python attendanceProject.py
   ```

3. The system will:
   - Load and encode all reference images
   - Access your webcam
   - Detect faces in the video feed
   - Compare detected faces with reference images
   - Mark attendance in attendance.csv when a match is found

## Attendance Record

The system generates an `attendance.csv` file with the following information:
- Name of the person
- Time of attendance

## Notes

- Ensure good lighting conditions for better face detection
- Use clear, front-facing photos for reference images
- The system automatically handles duplicate entries within the same day
