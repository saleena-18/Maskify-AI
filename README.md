# Maskify-AI

## Overview

Maskify AI is a Face Mask Detection System, a YOLOv7-based deep learning model trained to accurately recognize whether individuals in images and videos are wearing face masks or not. This system is deployed as a web application using Flask, enabling real-time mask detection through a user-friendly interface.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)

## Features

- Real-time face mask detection in images and videos.
- User-friendly web interface for uploading and processing files.
- Detailed performance metrics and visualizations.
- Efficient video compression and display.

## Installation

To set up the project locally, follow these steps:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/saleena-18/Maskify-AI.git
    cd Maskify-AI
    ```

2. **Create a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate
    ```

3. **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

4. **Download the trained model weights:**
    - Place the `best.pt` file in the `weights` directory.

5. **Run the Flask application:**
    ```bash
    flask run
    ```
## Model Training Process

### Training Phase:
- **Configuration Setup:** The model is trained using the `train.py` script with specified parameters for workers, batch size, epochs, image size, configuration file, dataset details, hyperparameters, and device allocation.
- **Model Training:** The YOLOv7 architecture is employed for 120 epochs, customized for the face mask detection task.

### Evaluation and Analysis:
- **Analysis and Metrics:** Post-training, the model's performance is evaluated using the `test.py` script, generating various metrics and visualizations like predictions, results, confusion matrices, and precision-recall curves.

### Inference and Deployment:
- **Model Deployment:** The trained model is utilized for real-time inference on images and videos using the `detect.py` script.
