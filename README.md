# Estimating Cosmological Parameters using Amortized Bayesian Inference

**Simulation-Based Inference for Cosmological Parameter Estimation**
Authors: Chandrae Roy · Riya Pinkeshbhai Prajapati · Neo Hong

---

## Overview

This project investigates the use of **Simulation-Based Inference (SBI)** and **Amortized Bayesian Inference (ABI)** for estimating cosmological parameters from the matter power spectrum. Traditional likelihood-based cosmological inference methods are computationally expensive and difficult to scale for high-dimensional simulations. To address this limitation, this project applies neural posterior estimation techniques to directly learn posterior distributions from simulated observations using deep learning models.

The primary objective of the project is to infer important cosmological parameters from noisy matter power spectrum observations while accurately quantifying uncertainty in the posterior distributions.

---

## Objectives

* Estimate cosmological parameters from simulated matter power spectrum data.
* Apply amortized Bayesian inference for efficient posterior estimation.
* Compare different neural network architectures for posterior inference.
* Evaluate calibration quality and predictive performance of inferred posterior distributions.
* Analyze uncertainty quantification in cosmological parameter estimation.

---

## Cosmological Parameters Estimated

The project focuses on estimating the following cosmological parameters:

| Parameter      | Description              |
| -------------- | ------------------------ |
| (H_0)          | Hubble constant          |
| (n_s)          | Scalar spectral index    |
| (\Omega_m h^2) | Matter density parameter |

---

## Dataset Generation

Synthetic matter power spectrum datasets were generated using the **CAMB (Code for Anisotropies in the Microwave Background)** cosmology package.

### Data Generation Process

* Defined physically motivated prior distributions for cosmological parameters.
* Simulated matter power spectra across different parameter combinations.
* Added Gaussian observational noise to create realistic cosmological observations.
* Generated training, validation, and testing datasets for posterior estimation models.

---

## Methodology

The project uses **Amortized Bayesian Inference (ABI)** through neural posterior estimation methods implemented in the **BayesFlow** framework.

### Inference Pipeline

1. Generate synthetic cosmological observations.
2. Train neural networks to learn mappings from observations to posterior distributions.
3. Approximate posterior distributions using normalizing-flow-based inference networks.
4. Evaluate posterior calibration and predictive accuracy.

---

## Models and Architectures

Multiple deep learning architectures were explored for posterior estimation.

### Summary Networks

* LSTM-based summary networks
* GRU-based summary networks

### Inference Networks

* CouplingFlow networks
* FlowMatching inference networks

These architectures were designed to efficiently capture complex relationships in high-dimensional cosmological data.

---

## Tools & Technologies

| Tool       | Purpose                               |
| ---------- | ------------------------------------- |
| Python     | Data processing and model development |
| BayesFlow  | Simulation-based inference framework  |
| CAMB       | Cosmological simulation generation    |
| TensorFlow | Deep learning implementation          |
| NumPy      | Numerical computation                 |
| Matplotlib | Visualization and diagnostics         |

---

## Model Evaluation

Model performance and posterior calibration were evaluated using multiple diagnostic techniques.

### Evaluation Methods

* Parameter recovery plots
* Simulation-Based Calibration (SBC)
* Posterior contraction analysis
* Posterior predictive diagnostics
* Calibration and uncertainty visualization

---

## Results

The trained models successfully recovered cosmological parameters from unseen simulated observations with strong agreement between predicted and true parameter values.

### Key Findings

* Neural posterior estimation effectively approximated posterior distributions for cosmological parameters.
* LSTM and GRU architectures demonstrated strong predictive performance.
* Simulation-Based Calibration indicated well-calibrated posterior estimates.
* Posterior contraction analysis showed meaningful uncertainty reduction from prior to posterior distributions.
* Hierarchical flow-based inference networks improved posterior flexibility and calibration quality.

The results demonstrate that amortized Bayesian inference provides a scalable and computationally efficient alternative to traditional likelihood-based cosmological inference methods.

---

## Limitations

* The study relies on simulated cosmological observations rather than real observational datasets.
* Only a limited set of cosmological parameters was estimated.
* Model performance may vary for higher-dimensional parameter spaces.
* Additional architectures and inference techniques could further improve posterior calibration and predictive accuracy.

