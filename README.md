# ECE-6023-Final-Project
AI-Powered 6G Beam Management Demo

## Overview
This repository contains a complete MATLAB-based pipeline for machine-learning-driven beam selection in a 28 GHz mmWave link. It includes:

1. **Dataset generation** (`generateDataset.mlx`)  
2. **MLP training & evaluation** (`trainBeamNet.mlx`)  
3. **Results:** a 10 000×256 feature dataset, a trained model, and evaluation plots  
4. **Report & slides** (in `/docs`) with methodology, results, and future work

---

## Prerequisites

- **MATLAB R2023b** or later  
  - **5G Toolbox**  
  - **Phased Array System Toolbox**  
  - **Deep Learning Toolbox**  
- A Live-Editor capable MATLAB license  
- (Optional) Git for cloning this repo  

---

## Repository Structure
## Files

- **generateDataset.mlx**  
  Live script that generates the 28 GHz beam-management dataset.

- **trainBeamNet.mlx**  
  Live script that trains and evaluates the MLP on that dataset.

- **beamDataset28GHz.mat**  
  The MATLAB `.mat` file produced by the generator (10000×256 features + labels).

- **docs/eg3573 ECE 6023 Final Project Report.pdf**  
  Final project report.

- **docs/6G_Beam_Management_Slides.pdf**  
  Final slide deck.

- **README.md**  
  This file.
