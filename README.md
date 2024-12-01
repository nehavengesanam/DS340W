# DS340W Project: AI-Generated vs. Human-Written Text Detection

## Overview
This repository contains code and resources for the DS340W final assignment, which investigates the effectiveness of AI-generated text detection models. The focus of this study is to evaluate how text length impacts detection accuracy. By utilizing pre-trained machine learning models and a curated dataset, this project contributes to understanding the challenges of AI detection accuracy in real-world scenarios.

## Research Objectives
1. To analyze the effect of text length on performance of AI detection models.
2. To compare detection accuracy for short (<50 words) versus long (>200 words) texts.
3. To provide insights for improving AI detection systems in academia, journalism, and social media.

## Code

The main Python script, DS340TESTING.py, performs the following tasks -

### Load and Preprocess Data:
Reads 340dataset.csv and categorizes texts into short and long lengths.

Splits the dataset into training (70%), validation (15%), and testing (15%) subsets.

### Apply the Detection Model:
Utilizes a pre-trained `roberta-base-openai-detector` model to classify texts as "AI-generated" or "Human-written."

Tokenizes texts using Hugging Face's `AutoTokenizer`.

### Evaluate Performance:

Outputs metrics such as - 
- Accuracy
- AUROC (Area Under the Receiver Operating Characteristic Curve)
- Precision, Recall, and F1 Score
- Confusion Matrix for classification performance.

## Code Implementation

1. Download Files:

Download the following files from this repository:
- `340detection.py`: Python script containing the code.
- `340dataset.csv`: Dataset used for analysis.

2. Upload Files to Google Colab:

Open [Google Colab](https://colab.research.google.com/) in your browser.

Create a new notebook and upload the `340detection.py` file.

Upload the `340dataset.csv` file to the Colab environment (using the file upload option).

3. Run the Code:

Run all the cells in the notebook.

4. What the Code Does:

## Results

## Acknowledgments


