# Expression Detection
This project uses FER (Facial Expression Recognition) and OpenCV to detect and analyze facial expressions in real time from a webcam feed. It identifies emotions such as happiness, sadness, anger, surprise, and more by analyzing facial features.

# Features
Real-Time Emotion Detection:
Processes live webcam input to detect facial expressions.
Emotion Analysis:
Identifies dominant emotions for each detected face in the video frame.
Visual Feedback:
Draws bounding boxes around faces and displays detected emotions with confidence scores.

# Installation
1. Clone the Repository
git clone https://github.com/nehaatri1997/expression-detetction/blob/main/Expression_detection.py
cd expression-detection
2. Install Required Libraries
Install the necessary dependencies:
pip install opencv-python tensorflow fer

# Usage
1. Run the Script
python expression_detection.py
2. Live Webcam Detection
The script will access your default webcam.
Detected emotions will be displayed as text above the faces, along with confidence scores.
3. Stop the Program
Press the 'q' key to exit the webcam feed and stop the program.

# File Structure
expression_detection/
│
├── expression_detection.py   # Main Python script for expression detection
└── README.md                 # Documentation file

# Customization
Adjust Webcam Input:
If you have multiple webcams, modify the line:
cap = cv2.VideoCapture(0)  # Change 0 to 1 or another index for different cameras
Emotion Label Colors:
Modify the cv2.putText function to use custom colors:
cv2.putText(frame, f"{emotion} ({score:.2f})", (x, y - 10),
            cv2.FONT_HERSHEY_SIMPLEX, 0.6, (255, 255, 255), 2)

# Limitations
The accuracy of emotion detection depends on lighting and camera quality.
Works best with frontal face angles; side profiles may not be detected accurately.

# Future Enhancements
Integration with text-based sentiment analysis for hybrid emotion detection.
Support for analyzing recorded video files in addition to live webcam feeds.
Add a GUI for better user experience and visualization.
