Markdown
# Saffron (Crocus sativus) Stigma Detection & Spatial Localization using YOLOv8

An automated computer vision pipeline designed for robotic saffron flower harvesting. This project fine-tunes a **YOLOv8** object detection model to accurately detect and segment saffron floral parts (stigmas/styles) and calculate their spatial center coordinates ($X_c, Y_c$) to guide robotic harvesting manipulators.

---

## 📌 Project Overview
Manual harvesting and stigma separation of saffron (*Crocus sativus L.*) is extremely labor-intensive. This project develops a vision-guided perception subsystem that:
- Detects saffron flower components (red stigmas, yellow stamens, purple petals) under variable illumination.
- Extracts target bounding boxes with high precision.
- Calculates pixel centroids ($X_c, Y_c$) and spatial bounding vectors for Cartesian harvesting end-effectors.
- Provides an intuitive Tkinter-based graphical user interface (GUI) for testing and visual verification.

---

## 📂 Repository Structure

```text
├── Saffron_Vision_Final_codes/     # Python scripts (Tkinter GUI, inference, centroid extraction)
├── Detection_Samples/              # Inference samples with bounding boxes & coordinates
├── Papers/                         # Reference literature on robotic saffron harvesting
└── README.md                       # Project documentation
🗃️ Dataset Notice
The dataset contains annotated high-resolution images of saffron flowers with bounding boxes around target stigmas.

Note: The proprietary training dataset and raw Roboflow annotations are kept private for ongoing academic research. The trained model weights and evaluation samples are documented in this repository for verification.

⚙️ Model & Training Pipeline
Architecture: Ultralytics YOLOv8

Input Resolution: 640 × 640

Training Platform: Google Colab GPU Runtime

Key Metrics: High mean Average Precision (mAP@0.5) optimized to minimize false negatives on delicate stigmas.

🚀 Getting Started
1. Prerequisites
Install required dependencies:

Bash
pip install ultralytics opencv-python pillow numpy
2. Running the GUI
To test the inference application and visualize centroid calculations:

Bash
python Saffron_Vision_Final_codes/main.py
(Use the GUI file picker to select an image from Detection_Samples/)

📊 Sample Detections
Sample outputs illustrating detected stigmas alongside computed center points are available in the Detection_Samples/ directory.

👨‍💻 Author
Soroush Shaftarouni

Department of Mechanical Engineering, Sharif University of Technology

Specialization: Dynamics, Control & Agricultural Robotics
