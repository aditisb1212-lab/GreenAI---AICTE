#GreenAI---AICTE
💧 CNN–LSTM Hybrid Model for Sustainable Water Usage Prediction
🧭 Project Overview

Efficient water management is one of the biggest sustainability challenges faced by modern cities.
Households often overuse or underutilize water due to a lack of awareness of actual needs influenced by environmental and behavioral factors.

This project leverages AI-driven forecasting to predict daily household water consumption based on environmental and household variables such as temperature, humidity, number of residents, and day of the week.
By providing accurate daily predictions, the model aims to help individuals and authorities optimize water usage, reduce waste, and plan sustainable resource strategies.

🌱 Problem Statement

Households often lack insights into how environmental and lifestyle factors affect water consumption.
Due to this, cities face inefficient water distribution and wastage, especially during heatwaves or peak hours.
The goal of this project is to predict next-day household water usage using the past 7 days of environmental and behavioral data.

🎯 Objectives

Predict next-day water consumption using previous daily records.

Analyze the influence of environmental parameters (temperature, humidity).

Develop a sustainable decision-support system for smart cities and households.

Demonstrate an explainable, data-driven approach to sustainable water management.

🧩 Dataset Description

The dataset contains (simulated or real) daily records with the following features:

Feature	Description
temperature	Daily average temperature (°C)
humidity	Daily average humidity (%)
num_residents	Number of people in the household
day_of_week	Coded from 0 (Monday) to 6 (Sunday)
water_usage	Total water used per day (liters)

📘 You can replace the simulated dataset with real data from municipal sources, IoT smart meters, or open sustainability datasets.

🧠 Model Architecture

This project uses a CNN–LSTM Hybrid Model built with TensorFlow/Keras.

🏗️ Architecture Flow:

1D CNN Layers

Detect local temporal patterns across short time windows (e.g., 2–3 days).

MaxPooling Layer

Reduces data dimensionality and captures dominant signals.

LSTM Layer

Captures long-term dependencies and weekly consumption patterns.

Dense Layers

Maps extracted features to a continuous output (predicted water usage).

⚙️ Model Summary
Layer	Type	Output Shape	Parameters
1	Conv1D (64 filters, kernel=2)	(None, 6, 64)	832
2	MaxPooling1D	(None, 3, 64)	0
3	LSTM (64 units)	(None, 64)	33024
4	Dense (64 units)	(None, 64)	4160
5	Dense (1 unit)	(None, 1)	65

Total Parameters: ~38K
Optimizer: Adam (LR=0.001)
Loss Function: Mean Squared Error (MSE)
Evaluation Metric: Mean Absolute Error (MAE)

🧮 Training and Evaluation

Epochs: 50

Batch Size: 16

Validation Split: 20%

Loss: Mean Squared Error (MSE)

Metric: Mean Absolute Error (MAE)

The model achieved stable convergence with low validation loss, demonstrating strong generalization to unseen days.

📊 Results and Visualization
🔹 1. Training vs Validation Loss

Shows model convergence and overfitting behavior.

🔹 2. Actual vs Predicted Water Usage

Displays how closely predicted usage follows real consumption patterns.

🔹 3. Next-Day Prediction Output

Example:

💧 Predicted next-day water usage: 421.56 liters

💡 Sustainability Impact

This project directly supports UN Sustainable Development Goal (SDG) 6 — Clean Water and Sanitation, by promoting:

Data-driven water conservation

Demand forecasting for water distribution

Smart city integration for sustainable resource management

With accurate forecasting, households can plan usage, and municipalities can minimize waste during high-demand periods.

🧰 Tech Stack
Category	Tools
Language	Python 3.10+
Libraries	TensorFlow, NumPy, Pandas, Scikit-learn, Matplotlib
Environment	Jupyter Notebook / VS Code
Model Type	CNN–LSTM Hybrid Regression Model
