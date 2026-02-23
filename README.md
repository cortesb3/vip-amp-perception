# VIP AMP Perception

## Overview
This repository contains computer vision work for autonomous vehicle perception, focusing on cone detection and synthetic data generation.

## Data Requirements
Before running any notebooks, download the following datasets from Google Drive:
- `AKS_cones/` - Cone detection dataset with images, masks, and labels
- `AMP_model_1.v2i/` - Background images for synthetic data generation  
- `GoKart_Images/` - Additional image dataset

## Fall Folder
The `fall/` directory contains work from last semester that was originally developed in Google Colab and has been migrated to run locally.

### Notebooks

**`cones.ipynb`**
- Integrates the SAM (Segment Anything Model) for cone segmentation
- Downloads and loads the 2.4GB SAM model checkpoint
- Provides interactive segmentation capabilities

**`crop_image.ipynb`**  
- Crops images using mask-based bounding boxes
- Processes cone images to extract regions of interest
- Handles alpha channel processing for clean cone assets

**`curating_coneData.ipynb`**
- Validates mask files and performs data quality checks
- Counts white pixels in masks to assess segmentation quality
- Helps curate the cone dataset for training

**`random_spawning.ipynb`**
- Generates synthetic training data by placing cone assets on background images
- Creates realistic cone placements with proper augmentation
- Outputs YOLO format annotations for training

### Files
- `sam_vit_h_4b8939.pth` - SAM model weights (2.4GB)

## Usage
1. Make sure all datasets are downloaded and placed in the project root
2. Run notebooks in the `fall/` folder to process cone data and generate synthetic datasets
3. Use the generated data for training autonomous vehicle perception models