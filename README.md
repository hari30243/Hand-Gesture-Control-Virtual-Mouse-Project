# Hand Gesture Controlled Virtual Mouse

A touchless virtual mouse application built using Python, OpenCV, MediaPipe, PyAutoGUI, and NumPy. This project allows users to control mouse movements, clicks, and scrolling using real-time hand gestures captured through a webcam.

## Features

- **Mouse Movement:** Move the index finger to control the cursor.
- **Vertical Scrolling:** Use two fingers to scroll up and down.
- **Horizontal Scrolling:** Use three fingers to scroll left and right.
- **Mouse Click:** Bring the index and middle fingertips close together to perform a click.
- **Stop Control:** Close all four counted fingers to stop mouse movement.
- **Real-Time Tracking:** Detect and track hand movements using MediaPipe.

## Technologies Used

- Python 3.12
- OpenCV
- MediaPipe
- PyAutoGUI
- NumPy

## Project Structure

```text
Hand-Gesture-Control-Virtual-Mouse/
│
├── main.py
├── README.md
└── report/
    └── Project_Report.pdf
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/hari30243/Hand-Gesture-Control-Virtual-Mouse-Project.git
```

### 2. Navigate to the Project Directory

```bash
cd Hand-Gesture-Control-Virtual-Mouse-Project
```

### 3. Create a Virtual Environment

```bash
py -3.12 -m venv venv
```

### 4. Activate the Virtual Environment

For Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### 5. Install Required Libraries

```bash
python -m pip install --upgrade pip
python -m pip install mediapipe==0.10.21 numpy==1.26.4
python -m pip install opencv-contrib-python==4.11.0.86 pyautogui
```

**Note:** Install only one OpenCV distribution to avoid conflicts between OpenCV packages.

### 6. Run the Application

```bash
python main.py
```

Your webcam will open, and the application will start detecting hand gestures.

## Gesture Controls

| Hand Gesture | Function |
|---|---|
| 1 Finger | Move Mouse |
| 2 Fingers | Vertical Scroll |
| 3 Fingers | Horizontal Scroll |
| 0 Fingers | Stop |
| Index + Middle Fingertips Close | Mouse Click |
| Press Q | Exit Application |

## How It Works

1. OpenCV captures live video from the webcam.
2. The captured frame is converted from BGR to RGB.
3. MediaPipe detects the hand and identifies its 21 landmarks.
4. The application counts extended fingers to identify gestures.
5. NumPy calculates fingertip positions and maps them to screen coordinates.
6. PyAutoGUI executes the corresponding mouse operations.
7. OpenCV displays the live camera feed and detected gesture status.

## Configuration

The following parameters can be modified in `main.py`:

| Parameter | Default Value | Description |
|---|---|---|
| CLICK_COOLDOWN | 1.0 | Delay between clicks |
| SCROLL_SPEED | 2 | Scrolling sensitivity |
| DEADZONE | 5 | Minimum movement threshold |
| max_num_hands | 1 | Maximum hands detected |
| Detection Confidence | 0.7 | Minimum detection confidence |
| Tracking Confidence | 0.7 | Minimum tracking confidence |

## Requirements

- Windows operating system
- Python 3.12
- Working webcam
- Proper lighting for accurate hand detection
- Required Python libraries

## Future Enhancements

- Improved gesture recognition accuracy.
- Cursor smoothing and sensitivity adjustment.
- Support for multiple hand gestures.
- Customizable gesture controls.
- Additional operations such as drag and drop.
- Improved user interface with real-time hand landmark visualization.

## Applications

- Touchless computer interaction.
- Accessibility support.
- Human-Computer Interaction (HCI).
- Gesture-based operating systems.
- Computer vision-based automation.

## Author

**Madupath Hari Haran**

## License

This project is developed for educational and demonstration purposes.
