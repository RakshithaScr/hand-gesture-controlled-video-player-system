# hand-gesture-controlled-video-player-system
# ✋ Hand Gesture Controlled Video Player System 🎬  
_A contactless multimedia control project using Arduino and Python_

This project allows users to control a video player using simple **hand gestures** detected by **ultrasonic sensors** connected to an **Arduino Uno**. The gestures are translated into media commands like play, pause, volume up/down, and scrolling — all automated through a Python script.

---

## 📽️ Demo Video

`/media/demo_video.mp4`

---

## 🔧 Features

- 🎥 Contactless media playback control
- 🤖 Integration of Arduino with Python automation
- 🎮 Supported actions:
  - ▶️ Play / ⏸️ Pause
  - 🔊 Increase / 🔉 Decrease Volume
  - ⏪ Rewind / ⏩ Forward
  - 🔼 Scroll Up / 🔽 Scroll Down
  - 🔵 Blue LED ON / 🔴 Red LED ON
- Real-time gesture detection using ultrasonic sensors

---

## 💻 Technologies & Libraries Used

### ✅ Arduino
- **Board**: Arduino Uno
- **Sensors**: HC-SR04 Ultrasonic Sensors (x2)
- **LEDs**: Blue and Red
- **Language**: C++ (Arduino)
- Key functions: `pulseIn()`, `digitalWrite()`, `Serial.println()`

### ✅ Python

| Library       | Purpose                                  |
|---------------|-------------------------------------------|
| `pyserial`    | Communicate with Arduino via serial port  |
| `pyautogui`   | Simulate keyboard/media control actions   |
| `os`          | Open video file with system default app   |
| `time`        | Add script delays                        |
| `opencv` *(optional)* | For future gesture recognition via webcam |

> Install Python dependencies:
> ```bash
> pip install pyserial pyautogui
> ```

---

## 🛠️ Tools Used

- **Arduino IDE** – Arduino code development and upload  
- **VS Code / Notepad** – Python code editing  
- **Tinkercad** – Circuit simulation (design only)  
- **Windows Media Player** – Default video playback  
- **Git & GitHub** – Version control and project hosting  

---

## 🚀 How to Run the Project

### 1. Upload Arduino Code
- Open `gesture_control.ino` in the Arduino IDE  
- Connect the Arduino Uno to your PC  
- Select the correct COM port and board  
- Upload the code

### 2. Connect the Hardware
- **Left Sensor**: Trig → D2, Echo → D3  
- **Right Sensor**: Trig → D4, Echo → D5  
- **Blue LED**: D8  
- **Red LED**: D9  
- Connect 5V and GND properly for all components

### 3. Run Python Script
- Open `video_control.py`
- Make sure:
  - The correct **COM port** (e.g. `COM4`) is set
  - The `video_path` points to a real `.mp4` video
- Run the script using:
```bash
python video_control.py
