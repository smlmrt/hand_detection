# Hand Tracking with MediaPipe

This project implements real-time hand tracking and gesture recognition using OpenCV and Google's MediaPipe library. It detects hand landmarks and classifies the state of the hand as "OPEN" or "CLOSE" based on finger positions.

## Features
- **Static Image Processing**: Detects hand landmarks in images and saves the annotated output.
- **Real-time Hand Tracking**: Uses webcam input to detect hands and track movements in real-time.
- **Gesture Recognition**: Determines whether a hand is open or closed based on the position of specific finger landmarks.

## Requirements
Make sure you have the following dependencies installed before running the script:

```bash
pip install opencv-python mediapipe
```

## How to Run
### Running on Static Images
1. Add image file paths to `IMAGE_FILES` in the script.
2. Run the script to process the images and generate annotated versions.

### Running in Real-Time (Webcam)
1. Ensure your webcam is connected.
2. Run the script:
   ```bash
   python hand_tracking.py
   ```
3. The script will open a window displaying the real-time hand tracking.
4. Press `ESC` to exit.

## How It Works
- The script initializes MediaPipe Hands for detecting and tracking hands.
- It processes each frame from the webcam and identifies hand landmarks.
- It calculates the relative position of the 9th and 12th hand landmarks.
- If the 12th landmark (middle finger tip) is below the 9th landmark (base of the middle finger), the hand is classified as "CLOSE"; otherwise, it is "OPEN".
- The classified state is displayed on the screen.

## Example Output
When the script runs, it will display:
- A live video feed with detected hand landmarks drawn.
- Text "OPEN" or "CLOSE" indicating the detected hand state.

## Future Improvements
- Enhance gesture recognition for more hand gestures.
- Add support for multiple hand gestures and actions.
- Optimize performance for mobile devices.

## License
This project is open-source and available under the MIT License.

