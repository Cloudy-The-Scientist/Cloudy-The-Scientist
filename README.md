![cloudy_banner](https://github.com/user-attachments/assets/2a76f2ca-01f0-42e3-b3d2-c4b1106e97c3)
# Cloudy The Scientist - Garbage Classification (Recyclable or Non-Recyclable)

## Project Goal

This project use the object detection to identify different types of waste. The goal is to help improve waste sorting and recycling by correctly classifying items.

## Files in this Repository

* `07 Cloudy The Scientist - Zero Waste_Final Report`: Final Project Report.
* `07 Cloudy The Scientist - Zero Waste_Final Presentation Slides.pdf`: Project presentation.
* `07 Cloudy The Scientist - Zero Waste_Proposal Slides.pdf`: Project Proposal Slides.
* `Cloudy-yolov8.ipynb`: Jupyter Notebook for YOLOv8 model training/evaluation.
* `Cloudy-supervision.ipynb`: Jupyter Notebook for running real-time waste classification using a webcam.
* `Dataset.zip`: The image dataset used for training and validation.
* `yolov8n.pt`, `yolov8m.pt`, `yolov8x.pt`: Pre-trained YOLOv8 model weights (nano, medium, extra-large).
* **Trained Models on '/runs' folder:**
    * The trained models are located at:
        * `runs/detect/train/weights/best.pt` as nano (n)
        * `runs/detect/train2/weights/best.pt` as medium (m)
        * `runs/detect/train4/weights/best.pt` as extra-large (x)
   
## Required Downloads (Dataset & Trained Models)

**IMPORTANT:** The image dataset (`Dataset.zip`), the pre-trained model folders (`runs/`) and PDF files are too large for GitHub. Please **download** them from the following link:
**Download Link:** [Cloudythescientist](https://studentmahidolac-my.sharepoint.com/:f:/g/personal/krerkkiat_wat_student_mahidol_ac_th/EtWXcdx-0zFEg2EyQHGmhrEB-8Q7xx-8nL2_r1iNGbAsMA?e=e6bpsx)

## Dataset

The model was trained on images from the "Recyclable and Household Waste Classification" dataset.

* **Source:** [Recyclable and Household Waste Classification Dataset on Kaggle](https://www.kaggle.com/datasets/alistairking/recyclable-and-household-waste-classification)
* **Classes Identified:**: ['BIODEGRADABLE', 'CARDBOARD', 'GLASS', 'METAL', 'PAPER', 'PLASTIC'].

## How to Run Real-Time Classification

1.  Making sure that you libraries installed (like OpenCV, PyTorch, Supervision, Ultralytics YOLO).
2.  Open and run the `Cloudy-supervision.ipynb` notebook.
3.  Use the `run_garbage_classifier` function within the notebook. Make sure your webcam is connected.

   ```python
   # Example using the medium model with 80% confidence threshold
   run_garbage_classifier(camera_index=0, model_type="m", conf=0.8)

   # Options:
   # model_type: "n", "m", or "x"
   # camera_index: 0, 1, etc. (depending on your system)
   # conf: Confidence threshold (e.g., 0.6 for 60%)
