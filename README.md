# AI-Enabled Smart Garbage Classification System 🗑️🤖

This project implements an **AI-Enabled Smart Garbage Classification System** on a **Raspberry Pi 3** to sort waste into categories (e.g., recyclable, organic, etc.). The system uses machine learning models to classify garbage in real-time, promoting sustainable waste management.

---

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Machine Learning Models](#machine-learning-models)
- [Setup and Installation](#setup-and-installation)
- [How It Works](#how-it-works)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## Overview
The **AI-Enabled Smart Garbage Classification System** is a Raspberry Pi-based solution that uses **machine learning** to classify garbage into categories. The system relies on pre-trained models deployed locally on the Raspberry Pi to process images captured from a connected camera.

In this project, we have developed and evaluated three models:
1. **Convolutional Neural Networks (CNNs)** for high accuracy and scalability.
2. **TensorFlow Lite Models** for efficient edge computing.
3. **[LOBE](https://lobe.ai/)**, a no-code AI platform, for ease of training and deployment.

We chose to use **LOBE** in this system for its simplicity in deployment and compatibility with Raspberry Pi 3.

---

## Features
- **Real-time image classification** of garbage.
- Runs efficiently on low-power hardware (**Raspberry Pi 3**).
- **User-friendly interface** for monitoring results.
- Easily trainable using the LOBE platform.
- Promotes environmental sustainability through proper waste segregation.

---

## Hardware Requirements
- **Raspberry Pi 3** (or higher)
- **Camera Module** (e.g., Raspberry Pi Camera v2)
- **Power Supply** for Raspberry Pi
- **SD Card** (16GB or more with Raspbian OS installed)
- A suitable **garbage container** for integration

---

## Software Requirements
- **Python 3.7+**
- **LOBE-trained model (.tflite format)**
- Required Python packages:
  - `tensorflow`
  - `numpy`
  - `opencv-python`
  - `pillow`
  - `flask` (if a web interface is required)

---

## Machine Learning Models
### Model Evaluation
We developed and tested the following models:
1. **Convolutional Neural Network (CNN)**: Achieved high accuracy but required significant resources.
2. **TensorFlow Lite**: Optimized for edge devices but required manual conversion and fine-tuning.
3. **LOBE**: No-code platform, simple training and deployment, compatible with Raspberry Pi.

### Model Used
For this project, we are using **LOBE** for its ease of training and seamless integration on Raspberry Pi.

---

## Setup and Installation
Follow these steps to set up the system on a Raspberry Pi:

### 1. Install Raspbian OS
- Install the **Raspberry Pi Imager** and flash the latest Raspbian OS onto the SD card.
- Boot the Raspberry Pi and ensure it’s connected to the internet.

### 2. Create a Python Virtual Environment
1. Open the terminal and install `virtualenv`:
   ```bash
   sudo apt-get install python3-venv

 
### 3. Create a virtual environment:

 ```bash

python3 -m venv garbage_env

####4. Activate the virtual environment:

 ```bash

source garbage_env/bin/activate
Upgrade pip and install required packages:

bash

pip install --upgrade pip
pip install tensorflow numpy opencv-python pillow flask
Deploy the LOBE Model
Train your garbage classification model using LOBE on your desktop.
Export the model in TensorFlow Lite (.tflite) format.
Transfer the model file (e.g., model.tflite) to the Raspberry Pi using scp or a USB drive.
Clone the Repository
Clone this GitHub repository on your Raspberry Pi:

bash

git clone https://github.com/yourusername/ai-smart-garbage-classifier.git
cd ai-smart-garbage-classifier
Run the Application
Run the classification script:

bash

python classify.py
How It Works
The Raspberry Pi camera captures an image of the garbage.
The image is processed by the LOBE-trained TensorFlow Lite model.
The system classifies the garbage into predefined categories (e.g., recyclable, organic).
Classification results are displayed on the terminal or a connected web interface.
Future Enhancements
Expand the model to classify additional waste categories.
Add robotic integration for automated sorting.
Develop a mobile app for real-time monitoring and user interaction.
Integrate with IoT platforms for smart city waste management.
License
This project is licensed under the MIT License. See the LICENSE file for more details.

Contributions 🤝
We welcome contributions! Feel free to submit issues, pull requests, or suggestions for improving this project. Together, let’s build a smarter and cleaner future! 🌍


