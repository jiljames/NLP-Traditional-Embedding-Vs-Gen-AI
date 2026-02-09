# ECE 219 Project 1: Comparing Text Embedding Methods for NLP Classification tasks

## Project Completed By
- Jillian James


## Academic Integrity Disclaimer:
This notebooks were created as part of Project 1 in ECE 219 at UCLA and uploaded with permission of the TA/Professor. If you use any part of this work in your own project for this class, you may be subject to disciplin ary action based on UCLA's academic integrity policy.


## Overview
Part 1 of this project implements and compares various text embedding methods (TF-IDF, GloVe, LLM encoders) for news article classification tasks. Part 2 compares how these methods perform on the PAWS dataset which is built adversarily. The ipynb files contain both the code for the project, as well as the written write-up portions of the project. 

## Files Structure
```
.
├── Project 1 Q1-Q14.ipynb          # Questions 1-14 (TF-IDF, GloVe, basic classification)
├── Project 1 Part 2 Q15-Q17.ipynb  # Questions 15-17 (PAWS dataset, Transformers)
├── Project1_Report_206556488        # Report as PDF
├── environment.yml                  # Conda environment file
├── requirements.txt                 # Pip requirements file
└── README.md                        # This file
```

## Setup Instructions

### 1. Environment Setup

Option A: Using Conda (Recommended)
```bash
conda env create -f environment.yml
conda activate ece219
```

Option B: Using pip
```bash
pip install -r requirements.txt
```

### 2. Download Required Datasets

**News Article Dataset:**
- Download from: [provided link in project]
- Place in the same directory as the notebooks
- Expected filename: `Project1-ClassificationDataset.csv`

**GloVe Embeddings:**
- Download from: https://nlp.stanford.edu/projects/glove/
- Download `glove.6B.zip` and extract
- Place the `glove` folder in the same directory as the notebooks
- Expected path: `glove/glove.6B.300d.txt`

### 3. Running the Notebooks

**For Questions 1-14:**
```bash
jupyter notebook "Project 1 Q1-Q14.ipynb"
```
Run all cells sequentially.

**For Questions 15-17:**
```bash
jupyter notebook "Project 1 Part 2 Q15-Q17.ipynb"
```
**Note:** This notebook requires GPU for reasonable runtime. Consider using Google Colab if local GPU is unavailable.

## Runtime Warnings
- **GridSearch (Q11)**: May take up to 4 hours to complete
- **Cross-encoder fine-tuning (Q17)**: Requires GPU, ~30-60 minutes with GPU
- **LLM inference (Q18)**: Requires GPU, ~10-20 minutes for 200 examples

## Random Seed
All experiments use `random_seed=42` as specified in the project requirements.

## Expected Directory Structure After Setup
```
.
├── Project 1 Q1-Q14.ipynb
├── Project 1 Part 2 Q15-Q17.ipynb
├── Project1-ClassificationDataset.csv
├── glove/
│   └── glove.6B.300d.txt
├── environment.yml
├── requirements.txt
└── README.md
```

## Troubleshooting

**"ModuleNotFoundError"**: Ensure all dependencies are installed from requirements.txt

**"File not found" errors**: Verify dataset paths match the expected structure above

**GPU/CUDA errors in Part 2**: Questions 17-18 require GPU. Use Google Colab or reduce batch size.

## Notes
- Part 1 (Q1-Q14) can run on CPU
- Part 2 (Q15-Q17) requires GPU for practical runtime
- All outputs and figures, and written results are provided within the notebooks
