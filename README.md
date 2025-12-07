# Face Recognition Pipeline (MediaPipe + LBPH)

A lightweight and practical face-recognition system combining:

- MediaPipe Face Mesh for face detection
- OpenCV LBPH for classical face recognition

This project provides a complete workflow: capture → train → recognize.

---

## Project Structure

project/
│── capture.py          # Capture and store face images
│── train.py            # Train the LBPH model
│── predict.py          # Real-time face recognition
│── dataset/            # Auto-created user image folders
│── models/
│     ├── lbph_model.xml
│     └── label_map.json
│── README.md

---

## 1. Capture Face Images

Run:

python capture.py

You will be asked to enter your name. Look into the camera and press Q to stop.

Images are saved in:

dataset/<your_name>/

---

## 2. Train the LBPH Model

Run:

python train.py

This generates:

models/lbph_model.xml
models/label_map.json

---

## 3. Real-Time Face Recognition

Run:

python predict.py

The webcam window will display:
- A green rectangle around the face
- The predicted name
- The LBPH confidence score

Press Q to exit.

---

## Installation

pip install opencv-python mediapipe
pip install opencv-contrib-python

---

## How to Use

git clone https://github.com/amani-patrick/Facial_recognition.git

cd Facial_recognition

python -m pip install mediapipe opencv-python

Then run:
1. python capture.py
2. python train.py
3. python predict.py

---

## Notes

- Works with any number of people.
- For each new user, repeat capture → train.