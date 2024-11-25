# IPL Score Prediction using DNN

This project builds a machine learning model to predict the final score of an IPL cricket match given specific input parameters like venue, batting team, bowling team, batsman, and bowler. It uses a neural network implemented with TensorFlow and Keras, trained on IPL data.

---

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Model Architecture](#model-architecture)
- [Usage](#usage)
- [Widgets-Based Prediction](#widgets-based-prediction)
- [Dependencies](#dependencies)
- [Results](#results)

---

## Overview

This project demonstrates:
- Data preprocessing using `pandas` and `sklearn`.
- Neural network implementation using Keras and TensorFlow.
- Interactive widgets for user input and real-time score prediction.

---

## Dataset

The dataset contains IPL match data, including the following features:
- Venue
- Batting Team
- Bowling Team
- Batsman
- Bowler
- Total runs scored

Features like `runs`, `wickets`, and other ball-by-ball statistics are excluded for simplicity.

---

## Preprocessing

1. **Feature Selection:** Dropped unnecessary features such as `date`, `runs`, `wickets`, and others.
2. **Encoding:** Used `LabelEncoder` to encode categorical features.
3. **Scaling:** Applied `MinMaxScaler` for feature scaling.
4. **Train-Test Split:** Split the data into training and testing sets (70-30 ratio).

---

## Model Architecture

A dense neural network built using Keras:
- **Input Layer:** Accepts 5 features.
- **Hidden Layers:** 
  - First layer: 512 neurons, ReLU activation.
  - Second layer: 216 neurons, ReLU activation.
- **Output Layer:** Single neuron, linear activation for regression.
- **Loss Function:** Huber Loss for robustness.
- **Optimizer:** Adam optimizer.

---

## Usage

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/yourusername/ipl-score-prediction.git
   cd ipl-score-prediction
