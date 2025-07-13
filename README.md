# ⚽ Player Tracking and Re-identification using YOLO11 and Deep SORT

This project tackles the task of tracking football players across video frames using **YOLO11** (a custom-trained version of YOLOv8) for object detection and **Deep SORT** for real-time object re-identification.

---

## 🎯 Objective

The goal is to:
- Detect football players in match videos
- Track them across frames with consistent IDs
- Re-identify players even after occlusion or scene exit
- Save the final annotated video with bounding boxes and IDs

---

## 🧠 What is YOLO11?

> **YOLO11** is a customized version of **Ultralytics YOLOv8**, specially trained for football player detection.  
It uses a `best.pt` model file that improves performance on football-specific angles, uniforms, and camera settings.

---





## 🚀 How It Works

1. `best.pt` (YOLO11) detects players in each video frame.
2. Deep SORT assigns unique player IDs and tracks them over time.
3. Output video is saved with consistent bounding boxes and ID overlays.

---

## 🔧 How to Run (Locally or in Colab)

### 🔹 Install Dependencies

```bash
pip install ultralytics opencv-python deep_sort_realtime
```

### 🔹 Load the Model and Run

```python
from ultralytics import YOLO
from deep_sort_realtime.deepsort_tracker import DeepSort

model = YOLO("best.pt")
# Load your video and run detection + tracking
```

---

## 📦 Requirements

- `ultralytics`
- `opencv-python`
- `deep_sort_realtime`
- Python >= 3.8

---

## 🎥 Sample Output

The video `output_reid.mp4` shows successful player detection and consistent re-identification using Deep SORT.

> ⚠️ If you can’t upload `output_reid.mp4` to GitHub, use Google Drive and paste the public link here.

---



## 📬 Author

**Subham Kumar Das**  
 
GitHub: [github.com/Subham9Kumar3Das](https://github.com/Subham9Kumar3Das)

---

## 📌 Notes

- This project was completed as part of the interview assignment at **Liat.AI**.
- "YOLO11" refers to a custom YOLOv8 model shared for the task.
- Model and logic are tailored for football player tracking scenarios.

---

## 🤝 Acknowledgment

Thanks to **Liat.AI** for providing the opportunity and dataset.  
Special thanks for the `best.pt` YOLO11 weights used in this assignment.

