# Knowledge-Guided Learning for Gas Turbine Dynamics

This project demonstrates a **Knowledge-Guided Learning (KGL)** approach for modeling the temporal dynamics of gas turbines. The framework incorporates **domain knowledge** into the learning process using multi-state constraints, enhancing prediction accuracy and physical consistency compared to traditional deep learning models.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset Description](#dataset-description)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)

---

## Overview

### Objective

To predict the electrical power generated by a gas turbine based on input control signals while ensuring predictions align with real-world dynamics:

1. **Baseline Model**: A Recurrent Neural Network (RNN) with LSTM layers.
2. **Knowledge-Guided Model**: Extends the baseline by adding domain knowledge through a custom multi-state constraint loss.

---

## Features

- Implements **Baseline** and **Knowledge-Guided Models**.
- Integrates **multi-state constraints** in loss functions for smooth and consistent predictions.
- Provides utilities to:
  - Preprocess time-series data.
  - Train models and evaluate performance.
  - Visualize results (loss curves, predictions vs ground truth).
- Demonstrates improved data efficiency and generalization.

---

## Dataset Description

The dataset consists of time-series data collected from a micro gas turbine and contains:

- **Columns**:
  - `time` (float64): Time steps.
  - `input_voltage` (int64): Control signal input.
  - `el_power` (float64): Electrical power output.
- **Files**:
  - `ex_1.csv` and `ex_9.csv` are used to combine training and testing data.

---

## Project Structure

   ─ data/ # Contains raw data files 
   ─ models/ # Stores trained models 
   ─ plots/ # Generated visualizations (e.g., loss curves, prediction plots) 
   ─ README.md # Project documentation 
   ─ preprocess.py # Data preprocessing script 
   ─ train_baseline.py # Script to train the baseline model 
   ─ train_kgl.py # Script to train the knowledge-guided model 
   ─ utils.py # Utility functions for evaluation and visualization

## Requirements

The project requires the following Python packages:

- `tensorflow`
- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`

Install them using:

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn


Setup Instructions
Clone the Repository:
bash
Copy code
git clone https://github.com/aum2606/gas-turbine-kgl.git
cd gas-turbine-kgl
```
