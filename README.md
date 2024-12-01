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


## Results

The `results.pdf` file is a direct copy of the output generated when running the `DS340TESTING.py` script on Google Colab using a Jupyter Notebook. It contains the result metrics, including Precision, Recall, F1 Score, and the confusion matrix, as well as other relevant performance insights. The file demonstrates the execution of the code and the evaluation of the detection model on the `340dataset.csv` dataset.

The results highlight distinct differences in the model's performance between long and short texts:

### Short Texts (<50 Words):
- Low Accuracy: The model struggled to classify short texts due to lack of context and linguistic features.
- High False Positives: Many human-written texts were misclassified as AI-generated, suggesting the model relied on superficial patterns and npt robust for short text analysis.
- Challenges: Short texts provide fewer clues for the model to differentiate AI-generated content, leading to poor Precision and Recall.

### Long Texts (>200 Words):
- High Accuracy: Longer texts performed significantly better, with much higher detection accuracy and AUROC scores.
- Low Misclassification: Richer context in long texts allowed the model to detect subtle inconsistencies in AI-generated content, reducing false positives and false negatives.
- Strength: The structured and detailed nature of long texts provides the model with more reliable features for classification.

## Project Structure
```DS340W-AI-Text-Detection/
├── DS340TESTING.py        # Main Python script for running the analysis
├── 340dataset.csv         # Dataset used for training, validation, and testing
├── README.md              # Documentation for the project
├── results.pdf            # Copy of Output Generated
```

## Acknowledgments
The dataset and initial insights were sourced from [The Imitation Game: Detecting Human and AI-Generated Texts in the Era of ChatGPT and BARD](https://paperswithcode.com/paper/the-imitation-game-detecting-human-and-ai) by Kadhim Hayawi, Sakib Shahriar, and Sujith Samuel Mathew.


