# Hand Gesture Control for Brightness and Volume

## Overview

This project uses computer vision and machine learning to create a system that allows users to control screen brightness and system volume through hand gestures. By leveraging the power of MediaPipe for hand tracking and recognition, along with OpenCV for image processing, this application provides an intuitive and innovative way to interact with your computer without touching any hardware controls.

## Features

- **Hand Tracking and Landmark Detection:** Utilizes MediaPipe to detect and track hand landmarks accurately in real-time.
- **Brightness Control:** Adjust screen brightness using the distance between specific landmarks on your left hand.
- **Volume Control:** Adjust the system volume using the distance between specific landmarks on your right hand.
- **Real-time Processing:** Captures video from the webcam and processes frames in real-time for smooth user interaction.

## Dependencies

- Python 3.x
- OpenCV
- NumPy
- MediaPipe
- screen-brightness-control
- pycaw
- comtypes

## How It Works

### Hand Tracking and Landmark Detection

The application uses MediaPipe's `Hands` module to detect and track hand landmarks. The module identifies key points on the hands and provides their coordinates.

### Brightness Control

The distance between the thumb and index finger on the left hand determines the brightness level. The distance is mapped to a range of 0 to 100, which corresponds to the screen brightness percentage.

### Volume Control

The distance between the thumb and index finger on the right hand is used to determine the volume level. This distance is mapped to the system's volume range and adjusted accordingly.

## Code Explanation

### Main Script (`main.py`)

The main script initializes the webcam, sets up the hand tracking model, and processes each frame in real-time to detect hand landmarks. Based on the detected landmarks, it adjusts the brightness and volume.

### Helper Functions

- `get_left_right_landmarks`: Extracts landmarks for the left and right hands.
- `get_distance`: Calculates the distance between two landmarks.
  
## Future Work

- Improve gesture recognition accuracy.
- Add support for more gestures to control other system functions.
- Implement a more user-friendly interface using Streamlit or Gradio.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or new features.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements

- [MediaPipe](https://mediapipe.dev/) for the hand tracking solution.
- [OpenCV](https://opencv.org/) for image processing.
- [pycaw](https://github.com/AndreMiras/pycaw) for audio control.

