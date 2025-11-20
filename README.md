# YOLOv10 for Prohibited Item Detection in X-ray Security Screening

This repository contains the implementation and evaluation of YOLOv10 models for detecting prohibited items in X-ray security imagery, using the FSOD (Few-Shot Object Detection) dataset.

## 📁 Project Files

### Core Implementation
- **`medium-and-large-yolov10-fsod.ipynb`** - Main training notebook implementing YOLOv10 medium and large models on FSOD dataset
- **`fsod-final-report-generator.ipynb`** - Evaluation notebook for model validation and performance analysis

### Documentation & Research
- **`yolov10 fsod report.pdf`** - Academic paper detailing the performance evaluation of YOLOv10 on X-ray security imagery
- **`Yolo v10.pdf`** - Comprehensive technical review of YOLOv10 architecture and innovations

## 🎯 Project Overview

This research evaluates the recently proposed YOLOv10 object detector for the specialized task of identifying prohibited items in X-ray security scans. The project assesses two model variants (YOLOv10-m and YOLOv10-l) on the comprehensive FSOD dataset, focusing on:

- NMS-free training strategy validation
- Performance comparison between medium and large models
- Real-world applicability for security screening

## 🏗️ Architecture Highlights

YOLOv10 introduces significant innovations:

- **NMS-Free Training**: Eliminates Non-Maximum Suppression through consistent dual assignments
- **Holistic Efficiency-Accuracy Design**: Optimized components for speed and accuracy
- **Spatial-Channel Decoupled Downsampling (SCDown)**
- **Partial Self-Attention (PSA)** for efficient global context modeling

## 📊 Dataset

**FSOD (Few-Shot Object Detection) Dataset**
- 20 classes of prohibited/notable items including:
  - Laptop, umbrella, mobile_phone
  - Various knives (straight_knife, folding_knife, utility_knife)
  - Security-risk items (lighter, battery, pressure_tank, etc.)
- Pre-divided into train/val/test splits

## 🚀 Implementation Details

### Models Trained
- **YOLOv10-m**: 16.5M parameters, 64.1 GFLOPs
- **YOLOv10-l**: 25.8M parameters, 127.4 GFLOPs

### Training Configuration
- **Epochs**: 60 for FSOD dataset
- **Image Size**: 640×640
- **Batch Size**: 16 (medium), 8 (large)
- **Hardware**: NVIDIA Tesla T4 GPU on Kaggle

## 📈 Results

### YOLOv10-m Performance
- **Validation**: mAP@50-95: 0.541, Precision: 0.817, Recall: 0.680
- **Test**: mAP@50-95: 0.541, Precision: 0.795, Recall: 0.703

### YOLOv10-l Performance  
- **Validation**: mAP@50-95: 0.559, Precision: 0.809, Recall: 0.709
- **Test**: mAP@50-95: 0.555, Precision: 0.818, Recall: 0.702

## 🔧 Usage

1. **Training**: Run `medium-and-large-yolov10-fsod.ipynb` for model training
2. **Evaluation**: Use `fsod-final-report-generator.ipynb` for performance validation
3. **Analysis**: Refer to the PDF reports for technical insights and comparative analysis

## 📚 Key Findings

- YOLOv10-l achieves superior performance (mAP@50-95: 0.559) while maintaining efficiency
- NMS-free architecture significantly reduces inference latency
- Models demonstrate strong generalization on unseen test data
- Effective for real-time security screening applications

## 🛠️ Dependencies

- Python 3.11+
- Ultralytics YOLO
- PyTorch
- OpenCV
- Other standard computer vision libraries

## 👨‍💻 Author

**Aryam E. Mersha** - Addis Ababa Science and Technology University

## 📄 License

This project is intended for academic and research purposes.
