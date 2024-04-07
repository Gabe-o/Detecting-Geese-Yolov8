# SE4442-Group-Project
Authors: Justin Chuang, Theodoros Kassa Aragie, Ahmad Abu Shawarib, and Gabriel Olivotto  
Course ID: CS4442B     
Instructors: Prof. Boyu Wang & Prof. Yalda Mohsenzadeh   
Date: 8 April 2024

Detecting Canadian Geese in images using YOLOv8.

## Project Structure
### benchmark
Benchmarks on the test set for various exports of the trained models on both the cpu and gpu

### data
Annotated dataset of goose images in YOLO format

### predict_images
Script for running prediction on images

### predict_video
Script for running prediction on videos

### test
Test results of the trained models on the test set

## training
- **baseline:** yolov8n, default settings (image size 640, and default data augmentation settings)
- **imgsz256:** yolov8n, image size set to 256
- **no_augmentation:** yolov8n, disabled all data augmentation
- **small:** yolov8s, default settings

## Hardware
OS: ubuntu 22.04    
CPU: Intel i7-9700k     
GPU: NVIDIA Telsa K80
