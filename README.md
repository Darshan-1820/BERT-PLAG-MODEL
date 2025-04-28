# BERT-PLAG-MODEL

## Overview
The BERT-PLAG-MODEL leverages a BERT-based model for detecting plagiarism in text documents. It classifies suspicious content based on various types of plagiarism, such as verbatim copying, paraphrasing, cross-language copying, and AI-generated content. The model uses BERT for sequence classification and is fine-tuned for this task.

## Features
Dataset Generation: Automatically creates synthetic datasets containing original and plagiarized text.

Plagiarism Detection: Provides a similarity score between two text samples to identify potential plagiarism.

Gradio Interface: A user-friendly web interface to test plagiarism detection.

## Requirements
To install required libraries:
pip install transformers datasets torch scikit-learn sentencepiece faker gradio

## Model Usage
Dataset Generation: Generates a dataset with randomly generated plagiarized text.

Preprocessing: Tokenizes text inputs for BERT model.

Training: Fine-tunes BERT on the dataset.

Plagiarism Check: Detects similarity and whether the text is plagiarized.

## Running the App
After training the model, launch the Gradio interface:
iface.launch()
This will start a local server where users can enter two texts for plagiarism checking.

## Working of the temporary model:
![image](https://github.com/user-attachments/assets/aefe0729-9ae5-4571-a47f-7d4f11d0e656)

The image showcases the Gradio interface where users can input an original and a suspicious text for plagiarism detection. The model calculates a similarity score, which indicates how similar the texts are. The threshold slider lets users set the minimum similarity required to flag the text as plagiarized. If the similarity score exceeds the threshold, the model marks the text as plagiarized ("Yes"); otherwise, it returns "No".

