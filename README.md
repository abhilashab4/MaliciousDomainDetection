# Malicious Domain Detection using image visualization and deep learning

## Overview

This project presents a novel cybersecurity approach by transforming structured DNS traffic data into visual representations. These images capture feature patterns within DNS queries, which are then analyzed by a custom Convolutional Neural Network (CNN) to detect malicious domains, including those used for malware, phishing, and botnets. By leveraging CNNs on visualized DNS data, the project overcomes limitations of traditional detection methods and identifies complex patterns in domain behavior.

## Problem Statement

Malicious domains are a major cybersecurity threat, often serving as entry points for attacks. Conventional detection techniques struggle with evolving threats and intricate DNS patterns. This project addresses these challenges by converting DNS traffic into images, enabling CNNs to detect subtle patterns that indicate malicious activity.

## Research Objectives

- Develop an image-based representation of DNS data, converting structured features into grayscale and RGB images for feature extraction.
- Design and train a custom CNN model to classify domains as malicious or non-malicious.
- Evaluate the effectiveness of deep learning models in detecting malicious domains.

## Implementation Details

### Data Preprocessing & Image Generation

- **Raw Data:** Structured DNS log files (e.g., `.csv`) containing features like domain length, numeric ratio, and entropy.  
- **Cleaning & Feature Engineering:** Used `pandas` and `NumPy` for cleaning, handling missing values, and feature engineering.   
- **Image Visualization:** Each row of DNS data is converted into a grayscale image, with each feature represented as a horizontal stripe whose intensity reflects the normalized value.  

### Model Training & Evaluation

- **CNN Architecture:** Custom CNN implemented in PyTorch, optimized for learning patterns in DNS images.  
- **Classification:** Binary classification of domains: "malicious" (Class 0) vs. "non-malicious" (Class 1).  
- **Metrics:** Model performance evaluated using Accuracy, Precision, Recall, and F1-Score.  
- **Results:** Achieved **97.8% accuracy** on the test set, demonstrating the effectiveness of image-based DNS analysis.
