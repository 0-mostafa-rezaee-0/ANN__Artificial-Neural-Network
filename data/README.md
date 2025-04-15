<div style="font-size:2.0em; font-weight:bold; text-align:center; margin-top:20px;">MNIST Data Directory</div>

# 1. Overview

This directory contains the MNIST dataset and samples for the artificial neural network project. The full MNIST dataset consists of 70,000 grayscale images of handwritten digits (0-9), with 60,000 for training and 10,000 for testing.

# 2. Directory Structure

```
data/
├── mnist/                # Contains the processed MNIST dataset (not included in git)
│   ├── X_train.npy      # Training images (60,000 × 28 × 28)
│   ├── y_train.npy      # Training labels (60,000)
│   ├── X_test.npy       # Test images (10,000 × 28 × 28)
│   ├── y_test.npy       # Test labels (10,000)
│   ├── X_train_flattened.npy  # Flattened training images (60,000 × 784)
│   └── X_test_flattened.npy   # Flattened test images (10,000 × 784)
└── mnist_samples/       # Contains sample images extracted from MNIST
    ├── digit_0_sample_1.png  # Individual sample images
    ├── digit_0_sample_2.png
    ├── ...
    └── mnist_samples.csv      # CSV with features of sample images
```

# 3. Data Files

## 3.1. MNIST Dataset (mnist/)

**Note**: The full MNIST dataset files are not included in the git repository due to their size. They will be generated when you run the `scripts/data_prep.py` script.

The dataset is preprocessed with the following steps:
- Images are normalized to have pixel values between 0 and 1
- Images are reshaped from 28×28 to 784-length vectors for the neural network

## 3.2. MNIST Samples (mnist_samples/)

This directory contains:
- 20 sample images for each digit (0-9), saved as individual PNG files
- A CSV file (`mnist_samples.csv`) with features calculated for each sample image

## 3.3. Sample CSV Structure

The `mnist_samples.csv` file contains the following columns:
- `digit`: The actual digit (0-9)
- `sample_id`: Sample number for that digit (1-20)
- `filename`: The corresponding image filename
- `mean_pixel`: Average pixel value (brightness)
- `std_pixel`: Standard deviation of pixel values
- `min_pixel`: Minimum pixel value
- `max_pixel`: Maximum pixel value

# 4. Generating the Data

To generate the MNIST dataset files:

```bash
python scripts/data_prep.py
```

To generate the sample images:

```bash
python scripts/extract_sample_images.py
```

# Data Folder

This folder contains datasets used in the Docker Data Science project.

## Contents

- `sample.csv`: A sample dataset containing mock data for experimentation and demonstration purposes. This file includes common data science features like numerical values, categorical data, and time-series information.

## Usage

Datasets in this folder can be accessed from within Docker containers as they are mounted as volumes. This allows you to:

1. Perform exploratory data analysis
2. Train machine learning models
3. Test data processing pipelines

## Best Practices

- Keep raw data separate from processed data
- Consider adding larger datasets to `.gitignore` and `.dockerignore`
- Document the source and structure of each dataset
- Use version control for datasets when appropriate 