# Detecting Geese with Yolov8
Authors: Gabriel Olivotto, Justin Chuang, Theodoros Kassa Aragie, and Ahmad Abu Shawarib   
Course ID: CS4442B     
Instructors: Prof. Boyu Wang & Prof. Yalda Mohsenzadeh   
Date: 8 April 2024

Detecting Canadian Geese in images using YOLOv8.

## [Report](Report.pdf)

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

### training
- **augmentation:** yolov8n, default settings (image size 640, and default data augmentation settings)
- **imgsz256:** yolov8n, image size set to 256
- **no_augmentation:** yolov8n, disabled all data augmentation
- **small:** yolov8s, default settings

## Hardware
OS: ubuntu 22.04    
CPU: Intel i7-9700k     
GPU: NVIDIA Telsa K80

## Reproducing Results
To reproduce the results found some changes will have to be made to various files in the codebase.
### config.yaml files
These are used by the YOLO package to define the location and settings used for training, validation, testing, and benchmarking.
it is very important that the `path` key contains the path from the root directory otherwise it will not work
### device settings
In many of the code files the you will see `device=[0,1]` this is configured to use GPU:0 and GPU:1 on the test machine if your machine does not contain multiple GPUs just set this to 0.
### Training times
In the current configuration on the hardware specified above training took anywhere from 30 minute to 2 hours.
