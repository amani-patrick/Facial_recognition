# Face Recognition Pipeline (MediaPipe + LBPH)

This project implements a full classical face-recognition pipeline using:

- **MediaPipe Face Mesh** : for face detection
- **OpenCV LBPH** : for feature-based face recognition

---

## 📂 Project Structure

project/
│── capture.py
│── train.py
│── predict.py
│── dataset/ 
│── models/ 
│ ├── lbph_model.xml
│ └── label_map.json
│── README.md


## 🚀 1. Capture Face Images

Run:

python capture.py

You will be asked:

Enter your name:

Then look at the camera.  
Press **Q** to stop capturing.

Images are saved to:

dataset/<your_name>/

---

## 🚀 2. Train the LBPH Model

Run:

python train.py

This will generate:

models/lbph_model.xml
models/label_map.json

---

## 🚀 3. Run Face Recognition

Run:

python predict.py

The camera window will show:

- A **green rectangle** around the face
- The **predicted name**
- The LBPH confidence score

Press **Q** to quit.


## Requirements

Install dependencies:

pip install opencv-python mediapipe
pip install opencv-contrib-python

---

## QUICK INFO!

This pipeline works with **any number of people**.  
Just repeat **capture → train → predict** and just enjoy the beauty of it.

## How to RUN

git clone