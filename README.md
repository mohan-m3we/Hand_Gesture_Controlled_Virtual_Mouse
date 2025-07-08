
---

# 🖐️ Hand Gesture Controlled Virtual Mouse

Hi, this is **mohan-m3we (Mohan M)** 👋
This project enables a user to control the computer mouse using hand gestures detected via a webcam — without touching the hardware! It supports two modes:

* **Bare hand tracking using MediaPipe**


---

## 📌 Project Features

* Cursor control with hand gestures
* Click (left, right, double) and scroll (vertical/horizontal) using pinch and finger gestures
* System volume and brightness control through pinch gestures
* Two gesture modes:

  * **Bare Hands** (`Gesture_Controller.py`)
 

---

## ⚙️ How to Run the Project

### 1. 📦 Prerequisites

Make sure the following libraries are installed:

```bash
pip install opencv-python mediapipe pyautogui screen_brightness_control comtypes pycaw
```

For the **Gloved Mode**, also install:

```bash
pip install numpy
```

---

### 2. ▶️ Running the Gesture Controller

Choose one of the following:

#### 🖐️ Mode 1: Bare Hand Gesture Controller

1. Open your IDE (e.g., PyCharm, VS Code)
2. Run:

```bash
python Gesture_Controller.py
```

> Uses MediaPipe to detect hands and gestures for mouse control and system functions.

---

#### 🧤 Mode 2: Gloved Hand Controller with ArUco Marker

1. Print and attach a **4x4 ArUco marker (DICT\_4X4\_50)** to your glove
2. Ensure calibration images are available in the `calib_images/checkerboard/` directory
3. Run:

```bash
python Gesture_Controller_Gloved.py
```

> This mode provides enhanced ROI detection and HSV masking using gloves and ArUco markers for gesture accuracy.

---

## 🖱️ Gesture Controls (Bare Hand Mode)

| Gesture              | Action                          |
| -------------------- | ------------------------------- |
| Fist                 | Left Mouse Drag                 |
| Palm (open hand)     | Cursor idle                     |
| Index Finger         | Right Click                     |
| Middle Finger        | Left   Click                    |
| Two Fingers (closed) | Double Click                    |
| Pinch (major hand)   | Brightness / Volume Control     |
| Pinch (minor hand)   | Horizontal / Vertical Scrolling |
| V Gesture            | Activate mouse movement         |

---

## 📂 Folder Structure

```bash
├── Gesture_Controller.py            # Main script for bare-hand gestures
├── Gesture_Controller_Gloved.py     # Glove + ArUco marker based controller
├── calib_images/
│   └── checkerboard/*.jpg           # Calibration images for camera
```

---

## 💡 Tips

* For **pinch gestures**, ensure both hands are visible to the webcam
* Use a well-lit environment for better accuracy
* Calibrate your camera properly for the gloved mode
* Press `Enter` (⏎) to exit the **bare-hand** mode or `q` to quit in **gloved** mode

---

## 🌟 Like This Project?

If you found this project helpful or interesting, please give it a ⭐️ on [GitHub](https://github.com/mohan-m3we/Hand_Gesture_Controlled_Virtual_Mouse) — your support means a lot!

---

