# Prenatal Down Syndrome Detection Using Deep Learning

## 🧠 Project Overview

This project focuses on automated prenatal screening for Down Syndrome using ultrasound fetal images. Specifically, it involves nuchal translucency (NT) length measurement using a deep learning pipeline that combines object detection and semantic segmentation using YOLOv11, and image processing techniques using OpenCV.

YOLOv11 implementation:
- Dataset was manually annotated using Roboflow by Ultralytics
- Pre-trained YOLOv11 model of medium size was loaded since it gives greater mAP at reduced processing time
- Binary masks are extracted with ROI in white color and background in black.

OpenCV:
- Extracted binary masks were used to measure vertical length of Nuchal Translucency
- Pixels were converted into mm to measure the length

Gradio:
- A simple UI for ease of use
- Users input ultrasound images and the results are detected ROIs with size and risk probability.

## 📂 Dataset

The dataset includes:

- **1528** annotated 2D ultrasound images from Shenzhen People’s Hospital
- **156** external validation images from the Longhua branch
- https://data.mendeley.com/datasets/n2rbrb9t4f/1
  
## 🧰 Technologies Used

- Python 3.12
- Roboflow (for data annotation)
- YOLOv11 (for object detection)
- Numpy (handling masks)
- OpenCV (for measurement)
- Gradio (for GUI)
- Google Colab
- Google Drive (for accessing and storing inputs and outputs)

## 📋 Results
- YOLOv11 effectively trains on the custom dataset and renders detected NT regions with near precision
- OpenCV generates and stores distinguishable binary masks which are easy to process and measures the their lengths through pixels
- Gradio acts like the frontend of the whole complexity of the project so that everyone can easily use the program without diving into the functionalities

## 🎥 Video Demonstration

