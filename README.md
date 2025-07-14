# 🚦 TrafficSignNet: Classifying German Traffic Signs with LeNet in Keras

![Traffic Signs](./images/traffic_signs.pngg)

> 🚗 **TrafficSignNet** is a deep learning project to classify German traffic signs into 43 distinct categories using a Convolutional Neural Network based on the classic LeNet architecture, implemented in Keras.  
> It uses the [German Traffic Sign Recognition Benchmark (GTSRB)](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset) dataset.

---

## 📚 Table of Contents
- [About the Project](#about-the-project)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [How to Run](#how-to-run)
- [Results](#results)
- [Examples](#examples)
- [References](#references)
- [License](#license)

---

## 🚀 About the Project

Traffic signs are essential for road safety. This project builds a robust classifier to automatically recognize traffic signs from images — a key component for autonomous driving systems and driver assistance technologies.

It applies the **LeNet-5 architecture**, originally designed for handwritten digit recognition, adapted to classify **43 types of traffic signs**.

---

## 🗂 Dataset

This project uses the [German Traffic Sign Recognition Benchmark (GTSRB)](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset), which includes:

- 🖼 **50,000+ images** of traffic signs.
- 📏 Resized to **32x32 RGB** (then converted to grayscale).
- 🚥 **43 classes** (e.g., Speed limits, Stop, Yield, Pedestrian crossing).

---

## 🧠 Model Architecture

The model is a modified **LeNet-5** CNN designed for multi-class traffic sign classification.

| Layer                | Details                           |
|----------------------|----------------------------------|
| **Input**             | 32x32x1 grayscale image          |
| **Conv2D + ReLU**     | 6 filters, 5x5, stride 1         |
| **AvgPooling**        | 2x2                              |
| **Conv2D + ReLU**     | 16 filters, 5x5, stride 1        |
| **AvgPooling**        | 2x2                              |
| **Flatten**           | → 400 neurons                    |
| **Dense + ReLU**      | 120 units                       |
| **Dense + ReLU**      | 84 units                        |
| **Dense + Softmax**   | 43 output classes               |

- **Loss Function:** `sparse_categorical_crossentropy`  
- **Optimizer:** `Adam`

---

## ⚙ Installation

1. **Clone this repository**

```bash
git clone https://github.com/keroti/TrafficSignNet.git
cd TrafficSignNet
