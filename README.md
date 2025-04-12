
# **Object Detection and Speed Estimation using YOLOv8**

This project focuses on detecting traffic objects (such as cars, buses, and trucks) and estimating their speeds from video footage using the **YOLOv8** object detection model. With integrated tracking and perspective transformation techniques, the system delivers annotated video output showcasing real-time object movement and estimated speed.

---

## 🚦 **Project Objectives**

- **Object Detection**: Identify and classify vehicles and other objects in traffic videos using YOLOv8.
- **Object Tracking**: Assign consistent IDs to detected objects across frames for accurate tracking.
- **Speed Estimation**: Calculate speed in km/h based on object displacement and frame rate, adjusted with perspective transformation.
- **Interactive Output**: Present results in an annotated, interactive interface using Gradio.

---

## ✨ **Key Features**

- **YOLOv8 Detection**: High-accuracy object detection with adjustable confidence and IoU thresholds.
- **ByteTrack Tracking**: Ensures consistent tracking IDs for each object across frames.
- **Perspective Transformation**: Custom mapping to convert pixel distance into real-world distance, improving speed accuracy.
- **Gradio Interface**: View results through an interactive, user-friendly web interface.

---

## 🧰 **Tech Stack & Requirements**

- **Programming Language**: Python 3.x
- **Libraries Used**:
  - [`ultralytics`](https://github.com/ultralytics/ultralytics) - YOLOv8 object detection
  - `OpenCV` - For video processing and drawing annotations
  - `NumPy` - For numerical computations
  - `ByteTrack` - For multi-object tracking
  - `Gradio` - For UI to display the annotated output

### 📦 Installation

Install all required dependencies using pip:

```bash
pip install ultralytics opencv-python numpy gradio
```

---

## 🛠️ **How to Use**

### 1. **Clone the Repository**
```bash
git clone <repository_url>
cd <repository_name>
```

### 2. **Run the Detection and Speed Estimation**
```bash
python main.py --input <path_to_traffic_video> --confidence <value> --iou <value>
```

- `<path_to_traffic_video>`: Path to the traffic video file.
- `--confidence`: Minimum confidence for YOLO detections (e.g., 0.5).
- `--iou`: IoU threshold to filter overlapping detections (e.g., 0.45).

### 3. **View Results**
After processing, the annotated video will open in a **Gradio interface**, showing:
- Bounding boxes around detected objects  
- Object labels and speed (in km/h)  
- Motion trace for each object  

---

## 🧩 **Core Components**

- **YOLOv8 Detector**: Frame-by-frame object detection using pretrained YOLOv8 weights.
- **Perspective Mapping**: Coordinate transformation to improve real-world distance estimation.
- **ByteTrack Tracker**: Assigns persistent IDs to each object to monitor movement across frames.
- **Speed Estimator**: Calculates speed based on movement over time, adjusted for perspective.
- **Gradio UI**: Lightweight interactive video playback embedded in a web interface.

---

## ⚙️ **Customization Tips**

- Adjust the `confidence` and `iou` parameters in the command line to fine-tune detections.
- Modify the perspective transformation matrix in the script to suit your camera angle.
- Extend the interface to export reports or speed logs for further analysis.

---

## 📄 **License**

This project is licensed under the **MIT License** — feel free to use, modify, and share it with attribution.

---

## 📬 **Contact**

**Developer**: *Rahul N*  
Feel free to reach out for questions, suggestions, or collaborations!

