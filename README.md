# Real-Time-Image-Classification-Model-Using-Edge-Impulse

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Edge Impulse](https://img.shields.io/badge/Built%20With-Edge%20Impulse-blueviolet)](https://www.edgeimpulse.com/)

An AI model, built with EDGE Impulse designed to classify what a camera is seeing in real life.

![Project Demo](assets/demo.gif)

## Table of Contents
* [About the Project](#about-the-project)
* [The Model](#the-model)
* [Technology Stack](#technology-stack)
* [Project Workflow](#project-workflow)
* [Getting Started](#getting-started)
* [Use Cases](#use-cases)
* [License](#license)
* [Acknowledgments](#acknowledgments)

## About the Project

This project demonstrates the accessibility of modern TinyML through a complete, end-to-end workflow. At its core is a custom-trained image classification model that runs entirely on-device—making it fast, private, and reliable without needing an internet connection.

The repository covers the full process: collecting data, training a model, and deploying it. Using platforms like Edge Impulse, building and deploying machine learning models at the edge is now approachable for anyone, not just experts.

## The Model

* **Task:** Real-Time Image Classification
* **Classifies:** Keys,Lamps,Unknown
* **Base Architecture:** Mobile Net V2 96x96
* **Public Edge Impulse Project:** [View the full project setup here](https://studio.edgeimpulse.com/public/772968/dashboard)

### Performance Metrics 
The model was optimized for on-device performance:
(Metrics for 32 bit quantised model)
|Metric            |Value          |
|----------------------------------|
|Testing Accuracy  |91.89%         |
|Latency           |7ms            |
|Ram               |893.7k         |
|Flash             |1.6M           |

## Technology Stack

* **ML Platform:** [Edge Impulse](https://www.edgeimpulse.com/) - Used for the entire workflow: data collection, training, optimization, and live testing.
* **Hardware:** Any modern **Smartphone** with a camera.
* **Interface:** A mobile **Web Browser** (like Chrome or Safari) to run the live classification.

## Project Workflow

**Data Acquisition –** In the Edge Impulse dashboard, a new device was added under the Devices tab. A smartphone was connected by scanning the project’s QR code, which allowed direct image capture from the phone’s camera. Using the Data Acquisition tab, multiple images of each item (such as a mug or a keyboard) were collected under different angles and lighting conditions to build a robust dataset.

**Labeling –** Each captured image was organized and labeled according to its class. For example, photos of mugs were grouped under the label mug, while keyboard images were grouped under keyboard. Proper labeling was critical for helping the model learn to distinguish between items.

**Impulse Design –** In the Impulse Design tab, an impulse was created by combining an Image processing block (for resizing and normalizing input data) with a Classification (Images) learning block, which is responsible for training the neural network.

**Training –** With the impulse set up, the model was trained in the cloud using Transfer Learning. This process fine-tuned a pre-trained MobileNetV2 model with the custom dataset, significantly reducing training time while improving accuracy.

**Deployment –** Once trained, the model was deployed to the connected smartphone through the Deployment tab. By scanning the QR code provided by Edge Impulse, the model was instantly accessible in the phone’s browser. This made it possible to test the classifier in real-world conditions, directly on the device, without requiring any additional setup.

## Getting Started

There are two ways you can get started with this project: testing the final, optimized model in your browser, or cloning the entire project to your own Edge Impulse account.

### Option 1: Test the Final Model (Quick & Easy)

This model has been deployed as a standalone web application, allowing you to run the fully optimized version directly in your phone's browser.

1.  **Open the Project:** Go to the public Edge Impulse project here: `https://studio.edgeimpulse.com/public/772968/dashboard`
2.  **Navigate to Deployment:** In the left-hand menu, click on the **Deployment** tab.
3.  **Build the Model:** Under 'Build firmware', find and select the **WebAssembly** option, then click the **Build** button. 
4.  **Scan the QR Code:** After a moment, a QR code will appear. Scan this with your smartphone's camera.
5.  **Start Classifying:** Your phone will open the web application. Grant it permission to use your camera and you can see the final model classify objects in real-time.

---
### Option 2: Clone the Full Project (For a Deeper Dive)

If you want to inspect the data, see the model settings, or train your own version, you can clone the entire Edge Impulse project.

1.  **Sign Up:** If you don't have one, create a free account at [Edge Impulse](https://www.edgeimpulse.com/).
2.  **Open the Project:** Go to the public Edge Impulse project here: `https://studio.edgeimpulse.com/public/772968/dashboard`
3.  **Clone:** At the top of the project dashboard, click the **Clone** button.
4.  **Explore:** The project, including its full dataset and model configuration, will be copied to your own account.

## Use Cases
* **Smart Homes:** Classifying if a room is 'occupied' or 'empty' based on the camera view.
* **Retail:** Analyzing a shelf to classify its status as 'fully stocked', 'low stock', or 'empty'.
* **Industrial Safety:** Classifying if a worker in front of a machine is wearing a 'hard hat' or 'no hard hat'.
* **Environmental Monitoring:** Classifying an image as containing 'recyclable plastic' or 'other waste'.
* **Agriculture:** Taking a picture of a leaf and classifying it as 'healthy' or 'diseased'.

## License

MIT License

Copyright (c) [2025] [Vision, MANIT]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Acknowledgments 
* The [Edge Impulse](https://www.edgeimpulse.com/) team for their fantastic platform.
* The participants of the Vision workshop.







