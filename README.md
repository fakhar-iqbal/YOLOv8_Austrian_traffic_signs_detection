# Traffic Signs Detection with YOLOv8

This repository contains code and resources for detecting Austrian traffic signs and signals using a YOLOv8 model. The project was built using Jupyter Notebooks and trained on the Austrian Traffic Signals Dataset (ATSD). This model aims to accurately detect and classify various types of traffic signs, aiding in applications like autonomous driving and traffic management systems.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Model](#model)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Results](#results)
7. [Acknowledgements](#acknowledgements)

---

## Project Overview

This project leverages YOLOv8 for detecting traffic signs and signals, trained on the Austrian Traffic Signals Dataset (ATSD). The goal is to achieve high accuracy in identifying traffic signals and signs, making it suitable for real-world applications requiring quick and precise detection.

## Dataset

- **Dataset Name**: Austrian Traffic Signals Dataset (ATSD)
- **Structure**:
  - The dataset contains images of Austrian traffic signs and their annotations.
  - Each image has an associated label file in YOLO format.
  - The data is organized into training and testing splits, defined in `train.txt` and `test.txt`.

## Model

- **Model Used**: YOLOv8
- **Framework**: PyTorch
- **Training Environment**: Google Colab

YOLOv8, known for its balance between speed and accuracy, is used in this project for detecting various traffic signs. The model was trained from scratch, using the configuration defined in the project notebook.

## Installation

1. **Clone the Repository**:
    ```bash
    git clone <repository-url>
    cd <repository-name>
    ```

2. **Install Requirements**:
    Run the following command to install all necessary packages:
    ```bash
    pip install -r requirements.txt
    ```

3. **Install YOLOv8**:
    If not installed, use the following command:
    ```bash
    pip install ultralytics
    ```

## Usage

1. **Load the Dataset**:
   Ensure that the dataset is properly organized, with `train.txt` and `test.txt` files listing training and testing images, respectively.

2. **Training**:
   Open the `YOLOv8_Traffic_Signs_Training.ipynb` notebook in Jupyter and run each cell to load data, configure the model, and start training. Customize training parameters such as batch size, epochs, and learning rate as desired.

3. **Inference**:
   To run inference on new images, use the inference section in the notebook to test the model's detection capability. You can also use command-line inference with:
    ```bash
    yolo task=detect mode=predict model=best.pt source=<image_path>
    ```

## Results

The model's performance is evaluated using metrics like mAP (mean Average Precision), precision, and recall on the test set. Sample predictions and detection results are included in the notebook to illustrate the model's effectiveness in identifying various traffic signs.

## Acknowledgements

- **Dataset**: Austrian Traffic Signals Dataset (ATSD)
- **YOLOv8 Framework**: [Ultralytics YOLO](https://github.com/ultralytics/ultralytics)

This project was developed for educational purposes and demonstrates the use of YOLOv8 in traffic sign detection.
