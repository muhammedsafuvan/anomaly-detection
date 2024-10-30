# Anomaly Detection with Robust Random Cut Forest (RRCF)

## Table of Contents
- [Overview](#overview)
- [Robust Random Cut Forest (RRCF) Algorithm](#robust-random-cut-forest-rrcf-algorithm)
  - [Effectiveness](#effectiveness)
- [Requirements](#requirements)
- [Installation](#installation)
- [Running the Code](#running-the-code)
- [Example Usage](#example-usage)
- [References](#references)

## Overview

This project implements real-time anomaly detection in data streams using the Random Cut Forest (RRCF) algorithm developed with Python 3.9.18. The code simulates a continuous data stream that includes seasonal patterns, trends, noise, and random anomalies. The RRCF algorithm is effective for identifying anomalies in high-dimensional data and is particularly well-suited for streaming data due to its efficiency and adaptability.

## Robust Random Cut Forest (RRCF) Algorithm

RRCF is an ensemble learning method designed for anomaly detection. It constructs a forest of binary trees where each tree is built by recursively partitioning the data space. The key idea behind RRCF is that normal points are expected to be surrounded by other normal points, while anomalies are more likely to be isolated.

### Effectiveness
- **Scalability**: RRCF can handle large datasets and streaming data efficiently.
- **Robustness**: It is resilient to noise and can adapt to changes in the data distribution over time.
- **Real-Time Processing**: RRCF allows for real-time anomaly detection, making it suitable for applications such as fraud detection, network security, and fault detection.

## Requirements
To run this code, you need Python 3.9 and the following Python packages

- `numpy`
- `matplotlib`
- `rrcf`
- `ipython`

See [requirements.txt](requirements.txt) for installation.

## Installation

1. Install Jupyter Notebook (if not already installed):
    ```
    pip install notebook
    ```

2. Launch Jupyter Notebook:
    ```
    jupyter notebook
    ```

3. Create a New Notebook: In your web browser, navigate to the Jupyter interface and create a new Python notebook.

4. Install required packages:
    ```
    !pip install -r requirements.txt
    ```

## Running the Code
This code is intended to be run in a Jupyter Notebook environment. Follow these steps to execute it:

1. Copy the provided anomaly detection code into a cell in your new notebook.

2. Execute the code cell. The program will start generating data in real-time and visualize it using Matplotlib.

3. View Results: The plot will update dynamically to show the data stream along with detected anomalies marked in red.

## Example Usage

You can customize the parameters for window_size and contamination when initializing the AnomalyDetection class:

`window_size = 100  # Size of rolling window for model training`
`contamination = 0.3  # Proportion of anomalies expected`
`detection = AnomalyDetection(window_size, contamination)`
`detection.real_time_plot()`


## References
RRCF Documentation
Original paper on RRCF algorithm: "Robust Random Cut Forest Based Anomaly Detection on Streams" by Guha, Mishra, Roy, et al.
