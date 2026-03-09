# COMSOL-Simulations-Experimental-Data
This repository contains a specialized dataset for Electrical Impedance Tomography (EIT) image reconstruction. It combines high-fidelity simulated data with real-world measurements acquired from a custom EIT device.  

📌 Overview
The goal of this dataset is to provide a robust foundation for training and validating EIT reconstruction algorithms. It bridges the gap between theoretical simulations and practical hardware acquisition.

Simulated Data: Generated using COMSOL Multiphysics.

Experimental Data: Acquired using the EIT device detailed in "Development and Validation of a Portable EIT System for Real-Time Respiratory Monitoring", https://doi.org/10.3390/s24206642.

📊 Data Structure
The dataset is organized into .npz files (NumPy compressed format). Each file represents a single data point consisting of the boundary voltage measurements and its corresponding conductivity distribution (image).
File Contents
Each .npz file contains two primary arrays:
1. Signal ($208 \times 1$): A vector containing the voltage measurements (or differential voltages) extracted from the EIT sensors.
2. Image ($60 \times 60$): A matrix representing the 2D cross-sectional reconstruction or the ground truth conductivity map.

🛠 Methodology
1. COMSOL Simulations
The simulated portion of the dataset was created by modeling a toraxic tank with 16 electrodes in COMSOL. We varied the size, position, and conductivity of inclusions to ensure diversity in the training set.

2. Experimental Acquisition
Real-world data was gathered using the hardware setup described in the associated paper. This data includes inherent noise and electrode contact impedance variations, providing a realistic challenge for reconstruction models. Also, the data were hand digitilized.
