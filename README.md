This project demonstrates real-time hand tracking using OpenCV and cvzone. It overlays and dynamically scales an image on the live webcam feed based on the distance between the index fingertips of two hands.

Overview

The script captures video from your webcam and uses cvzone's HandDetector to detect hand gestures. When two hands are detected with both showing the [1, 1, 0, 0, 0] gesture (indicating the index and middle fingers are up), it calculates the distance between the index fingertips. This distance determines the scaling of a loaded image, which is then overlaid onto the video stream. The processed video is saved as output_video2.mp4.

Features

Real-time Hand Detection: Utilizes cvzone's HandDetector for detecting and tracking hands.

Dynamic Image Scaling: Adjusts the size of an overlay image based on the distance between the index fingertips.

Interactive Overlay: Positions the overlay image at the center between the two index fingertips.

Video Recording: Saves the augmented video output locally.

Prerequisites

Python 3.x

OpenCV: For video capture, image processing, and display.

cvzone: For simplified hand detection and tracking.

Installation

Clone the Repository

bash
Copy
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
Install Dependencies

Install the required Python packages using pip:

bash
Copy
pip install opencv-python cvzone
Overlay Image

Make sure you have an image named IMG_3079.png in the project directory. This image will be used as the overlay.

Usage
Run the Script

Execute the Python script:

bash
Copy
python script_name.py
Replace script_name.py with the actual filename of your script.

Interact

The webcam window will open, showing the live video feed.

When you position two hands with the gesture [1, 1, 0, 0, 0] (index and middle fingers up) in view, the script calculates the distance between the index fingertips.

The overlay image (IMG_3079.png) is resized dynamically based on this distance and is placed at the calculated center point.

Press the 'q' key to exit the application.

Output Video

The processed video is saved as output_video2.mp4 in the project directory.

File Structure

bash
Copy
├── IMG_3079.png         # Overlay image file
├── script_name.py       # Main Python script (replace with your actual filename)
└── README.md            # This README file
How It Works

Video Capture: Uses cv2.VideoCapture(0) to capture video from the default webcam.

Hand Detection: The HandDetector from cvzone processes each frame to detect hands and the state of each finger.

Gesture Recognition: Checks for the specific gesture ([1, 1, 0, 0, 0]) on both hands.

Distance Calculation: Determines the distance between the index fingertips to set the scaling factor.

Image Overlay: Resizes the overlay image based on the calculated scale and blends it into the video frame.

Video Saving: Writes the augmented frames to a new video file (output_video2.mp4).

Troubleshooting

Image Not Found Error:

Ensure IMG_3079.png is present in the same directory as the script.

Webcam Issues:

Verify that your webcam is properly connected and not used by another application.

Dependency Issues:
Make sure all dependencies (opencv-python, cvzone) are installed correctly via pip.

Contributing
Contributions are welcome! Feel free to fork the repository and submit pull requests. For any major changes, please open an issue first to discuss what you would like to change.
