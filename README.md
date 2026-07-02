# Wind Turbine Multi-Fault Detection and Root Cause Analysis
[![Open In Colab]([https://colab.research.google.com/assets/colab-badge.svg](https://colab.research.google.com/drive/1npeUtciFzaFBblMKshx7EuTDhKL1RWbW?usp=sharing))](Link-to-your-colab-file-in-github)

## 📌 Overview
Wind turbines require robust problem detection techniques to guarantee optimal performance and prevent costly downtime. This project implements a novel method for identifying multiple faults and determining the underlying causes in wind turbines. It accomplishes this by utilizing multivariate time series data and a model based on autoencoders to differentiate between normal operational anomalies and actual malfunctions. 

## 🔬 Based On
The methodologies and algorithms implemented in this repository are based on the research presented in:
* **Title:** Multi fault detection and root cause analysis of wind turbine using Multivariate time series data based on autoencoder
* **Authors:** Manisha Galphade, Valmik Nikam, Biplab Banerjee, Nilkamal More, Arvind W. Kiwelekar, Priyanka Sharma
* **Journal:** Engineering Applications of Artificial Intelligence 176 (2026) 114700

##  Dataset
This project utilizes a custom 4 MB dataset included directly in this repository. It is based on wind turbine Supervisory Control and Data Acquisition (SCADA) system data.
* **Historical Context:** The underlying research utilized the Kelmarsh wind turbine dataset, comprising SCADA data for five 2 Mega Watt (MW) wind turbines from 2016 to 2021.
* **Features:** The data processing relies on 15 performance monitoring variables, including gear oil inlet pressure, generator bearing temperatures, wind speed, and active power.

##  Methodology & Tech Stack
* **Language:** Python
* **Environment:** Google Colab
* **Data Cleansing:** Multivariate Kernel Density Estimation (KDE) is utilized to detect and eliminate anomalous data points, preserving only the normal normative patterns.
* **Autoencoder Architecture:** The autoencoder was explicitly developed to acquire knowledge about the standard operational patterns of the wind turbine by analyzing historical data. 
* **Detection Process:** The model lowers the dimensionality of the data and recreates it; anomalies are then discovered based on reconstruction errors.

##  How to Run
The easiest way to run this project is directly through Google Colab.
1. Click the "Open in Colab" badge at the top of this README.
2. Run the cells sequentially. 
3. *Note: The notebook is configured to read the dataset directly from this repository's raw URL, so no local downloading is required.*

##  Results & Key Findings
* **Accuracy:** The proposed method achieved 94% precision, 93% recall, and an F1 score of 0.93.
* **False Positives:** The model demonstrated a highly efficient 5% false-positive rate.
* **Critical Detections:** When tested on SCADA data, the method successfully detected over 95% of critical wind turbine faults, including severe gearbox and generator issues.
* **Root Cause Analysis:** The framework provides insights into the underlying reasons for detected faults by examining the reconstruction error associated with individual input features, aiding in strategic operational decision-making.
