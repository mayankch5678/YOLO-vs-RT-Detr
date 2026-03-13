# YOLO vs RT-DETR on Endoscope Dataset

A comparative analysis of two state-of-the-art object detection architectures — **YOLOv8** and **RT-DETR** — evaluated on an endoscopic imaging dataset. This notebook explores how transformer-based detection compares against the YOLO family in a medical imaging context.

---

## Overview

Endoscopic image analysis is a challenging computer vision task due to variable lighting, motion blur, and subtle lesion features. This project benchmarks YOLO and RT-DETR to assess which architecture is better suited for real-time detection in clinical environments.

---

## Dataset

| Property | Details |
|---|---|
| Source | Kaggle / UCI (public) |
| Domain | Medical endoscopy |
| Task | Object detection |
| Format | Images with bounding box annotations |

> **Note:** See the [Dataset](#-dataset-setup) section below for download instructions.

---

## Models Compared

### YOLOv8
- Single-stage anchor-free detector
- Optimized for real-time inference
- Lightweight and fast

### RT-DETR (Real-Time Detection Transformer)
- Transformer-based encoder-decoder architecture
- No NMS (Non-Maximum Suppression) required
- Strong on complex scenes

---

## Results

| Model | mAP@50 | Inference Speed | Parameters |
|---|---|---|---|
| YOLOv8 | — | — | — |
| RT-DETR | — | — | — |

> Fill in results after running the notebook. Key metrics to compare: mAP@50, FPS, and model size.

---

## Installation & Setup

### Requirements

```bash
pip install ultralytics
pip install torch torchvision
pip install opencv-python matplotlib pandas
```

### Run in Google Colab (recommended)

Click the **Open in Colab** badge at the top of this README. No local setup required.

### Run locally

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
pip install -r requirements.txt
jupyter notebook
```

---

## Dataset Setup

1. Download the dataset from Kaggle:
   ```bash
   kaggle datasets download -d DATASET_NAME
   unzip DATASET_NAME.zip -d data/
   ```
2. Place the data in the following structure:
   ```
   data/
   ├── images/
   │   ├── train/
   │   └── val/
   └── labels/
       ├── train/
       └── val/
   ```
3. Update the dataset path in the notebook if running locally.

---

## Repository Structure

```
├── notebook.ipynb        # Main analysis notebook
├── README.md             # This file
├── requirements.txt      # Python dependencies
└── data/                 # Dataset (not tracked by git — see .gitignore)
```

---

## References

- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- [RT-DETR Paper](https://arxiv.org/abs/2304.08069)

---

## License

This project is open-source and available under the [MIT License](LICENSE).
