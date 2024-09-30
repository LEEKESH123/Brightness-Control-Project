# Brightness-Control-Project

Here's an example of a **README** file for your **Brightness Control with Hand Detection** project:

---

# BrightnessControlProject

## Overview
The **Brightness Control with Hand Detection** project allows users to adjust their screen's brightness using hand gestures, such as moving their thumb and index finger apart or closer together. This project uses **OpenCV**, **Mediapipe**, and **screen-brightness-control** to track hand movements and change the brightness in real-time.

## Features
- Real-time hand gesture detection using a webcam.
- Adjust screen brightness by detecting the distance between the thumb and index finger.
- Uses **Mediapipe** for hand tracking and **screen-brightness-control** to adjust screen brightness on Windows.

## Technologies Used
- **Python**
- **OpenCV**: For image processing and webcam access.
- **Mediapipe**: For hand gesture detection and tracking.
- **screen-brightness-control**: For adjusting the screen brightness on Windows.

## Prerequisites
Before running the project, ensure you have the following installed:

- Python 3.x
- The required Python libraries:
  - `opencv-python`
  - `mediapipe`
  - `screen-brightness-control`
  - `numpy`

You can install these libraries using the following commands:
```bash
pip install opencv-python mediapipe screen-brightness-control numpy
```

## How It Works
1. The webcam captures live video of the user's hand.
2. Mediapipe identifies hand landmarks and tracks the thumb and index finger.
3. Based on the distance between the thumb and index finger, the program calculates the brightness level using `np.interp()` to map the distance to a brightness value (0-100).
4. The screen brightness is adjusted in real-time using the `screen-brightness-control` library.

## Usage

1. Clone the repository or download the project files.
2. Install the required libraries by running:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Python script:
   ```bash
   python brightness_control.py
   ```
4. Move your thumb and index finger apart to increase brightness and closer together to decrease brightness.
5. Press **'q'** to exit the program.

## Code Explanation
The main components of the code include:

- **Hand Detection**: Mediapipe tracks the position of the thumb and index finger landmarks.
- **Distance Calculation**: The distance between these two landmarks is calculated using the `hypot` function.
- **Brightness Control**: The distance is mapped to a brightness level (0-100) using `np.interp()`, and the screen brightness is adjusted in real-time using the `screen-brightness-control` library.

## Screenshots
![Demo of Hand Gesture Brightness Control](assests/Screenshot (212).png)

## Potential Improvements
- Add more gestures for different actions like volume control.
- Improve accuracy for different lighting conditions or complex backgrounds.
- Expand the system to work with other operating systems (Linux, Mac).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Credits
- **Mediapipe**: Hand tracking model.
- **OpenCV**: Video capture and image processing.
- **screen-brightness-control**: For controlling the screen brightness in Python.

---

This README gives an overview of the project, setup instructions, and a brief explanation of how the code works. You can modify it to better fit your specific project setup and details.
