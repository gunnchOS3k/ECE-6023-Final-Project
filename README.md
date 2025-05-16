# AI-Powered 6G Beam Management Demo

## Overview
This repository contains a complete MATLAB pipeline for machine-learning-driven beam selection in a 28 GHz mmWave link:

1. **Dataset generation** (`generateDataset.mlx`)  
2. **MLP training & evaluation** (`trainBeamNet.mlx`)  
3. **Results**:  
   - 10 000×256 feature dataset  
   - Trained MLP model  
   - Evaluation plots  
4. **Report & slides** (in `docs/`)

## Files

- **generateDataset.mlx**  
  Live script that generates the 28 GHz beam-management dataset.

- **trainBeamNet.mlx**  
  Live script that trains and evaluates the MLP on that dataset.

- **beamDataset28GHz.mat**  
  MATLAB `.mat` file produced by `generateDataset.mlx` (10 000×256 features + labels).

- **docs/eg3573 ECE 6023 Final Project Report.pdf**  
  Final project report.

- **docs/6G_Beam_Management_Slides.pdf**  
  Final slide deck.

- **README.md**  
  This file.

## Prerequisites

- **MATLAB R2023b** or later with:
  - 5G Toolbox  
  - Phased Array System Toolbox  
  - Deep Learning Toolbox  
- Live Editor enabled

## Running the Project

1. **Open MATLAB** and navigate to this repo’s root folder.

2. **Generate the dataset**  
   - Open **generateDataset.mlx** in the Live Editor.  
   - Click **Run**.  
   - You should see in the Command Window:
     ```
     ✅ Generated beamDataset28GHz.mat
        features size = [10000 256]
        unique labels = 64
     ```
   - Confirm that **beamDataset28GHz.mat** appears in your folder.

3. **Train & evaluate the MLP**  
   - Open **trainBeamNet.mlx** in the Live Editor.  
   - Click **Run**.  
   - Watch the **training-progress** plot (loss & accuracy).  
   - In the Command Window, note a line like:
     ```
     🏁 Test Accuracy: XX.XX%
     ```
   - A **confusion matrix** figure will also pop up.

4. **Review results**  
   - Open `docs/6G_Beam_Management_Report_v4.pdf` for the full write-up.  
   - Open `docs/6G_Beam_Management_Slides_v4.pptx` for the slide deck.

## Key Results

- **Baseline Test Accuracy**: ~2.07 % (chance = 1/64 ≈ 1.56 %)  
- **Interpretation**: Random i.i.d. channels contain no spatial structure to learn.

## Future Work

- Integrate realistic TDL-D channel models (`nrTDLChannel`)  
- Add feature engineering (e.g. magnitudes, PCA)  
- Hyperparameter tuning & regularization  
- Explore 100 GHz THz-band extensions  
- Incorporate mobility for beam tracking

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgments

- Prof. S. Rangan’s MATLAB 5G Toolbox tutorials (NYU Tandon, Spring 2025)  
- MathWorks documentation for 5G Toolbox, Phased Array Toolbox, and Deep Learning Toolbox  
