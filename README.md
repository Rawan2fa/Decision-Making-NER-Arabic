# Decision-Making-NER-Arabic

## Overview
This project was developed as part of the Natural Language Processing course (CAI350)
at Princess Nourah bint Abdulrahman University.

It focuses on building an Arabic Named Entity Recognition (NER) system using AraBERT
to extract key entities from political texts and support decision-making
in governmental and diplomatic contexts.

## Problem Statement
Political texts such as speeches, letters, and official reports contain critical
information that is difficult to process manually at scale.
This project automates the extraction of key entities to improve efficiency
and accuracy in political text analysis.

## Dataset
- Source: iSemantics/conllpp-ner-ar (Hugging Face)
- Language: Arabic
- Annotation scheme: BIO
- Splits:
  - Train: 10,250 samples
  - Validation: 2,383 samples
  - Test: 2,572 samples

## Model & Approach
- Model: AraBERT (Transformer-based)
- Task: Named Entity Recognition (Token Classification)
- Preprocessing:
  - Text cleaning & normalization
  - Subword tokenization using AraBERT tokenizer
  - BIO label alignment
- Training:
  - Fine-tuning using Hugging Face Trainer
  - Optimizer: AdamW
  - Epochs: 5

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score (Entity-level)

### Results (Test Set)
- Accuracy: 94.38%
- Precision: 81.80%
- Recall: 82.77%
- F1-score: 82.26%

The model performed strongly on PER, ORG, and LOC entities,
with lower performance on MISC due to class imbalance.

## Demo & Interface
A simple web-based interface was implemented and exposed using Ngrok
to demonstrate real-time entity extraction from Arabic political texts.

## Tech Stack
- Python
- PyTorch
- Hugging Face Transformers
- AraBERT
- SeqEval
- Google Colab

## My Role
- Preprocessed Arabic text data to improve training readiness (cleaning & normalization).
- Ensured token/label consistency for BIO tagging before training.
- Performed train/validation/test splitting to support fair evaluation and generalization checks.


## Academic Note
This project was developed for academic purposes as part of a university course.
