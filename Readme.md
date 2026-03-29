# Edith.AI - Focus Detection System

A real-time computer vision application that monitors your focus and detects distractions during work or study sessions.

## Features

- **Real-time Face Detection**: Uses Haar Cascade classifiers to detect faces via webcam
- **Eye Detection**: Identifies when eyes are open and looking at the screen
- **Focus Monitoring**: Tracks three states:
  - **FOCUSED**: Eyes detected and looking at screen (green)
  - **WRITING/READING**: Face detected but eyes not visible (orange)
  - **DISTRACTED**: No face detected for extended period (red)
- **Audio Alerts**: Plays system sounds when distractions are detected
- **Visual Feedback**: Real-time display with status messages and visual indicators

## Requirements

- Python 3.x
- OpenCV (`opencv-python`)
- Windows (for `winsound` module)

## Installation

1. Clone or download this repository
2. Install dependencies:
```bash
pip install opencv-python
```

## Usage

Run the application:
```bash
python edith.py
```

or

```bash
python first.py
```

**Controls:**
- Press `q` to quit the application

## Configuration

Adjust these thresholds in the code to customize behavior:
- `MISSING_THRESHOLD`: Time in seconds before alerting when face is not detected (default: 2.0 seconds)
- `WRITING_THRESHOLD`: Time in seconds before alerting during writing/reading mode (default: 30.0 seconds)

## How It Works

1. Captures video from your webcam
2. Detects faces in each frame using pre-trained Haar Cascade classifiers
3. Analyzes the upper half of detected faces for eye regions
4. Classifies your focus state based on eye detection
5. Provides visual and audio feedback when distraction is detected

## Output Display

- **Green**: FOCUSED - Keep up the good work!
- **Orange**: WRITING/READING - Working on something
- **Red**: DISTRACTED - Refocus on your task!

