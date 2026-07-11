## Project Overview
Identifying the composer of a piece of music is an intricate task, historically requiring expert musicological knowledge. This project leverages deep learning architectures to automate the classification of musical scores. By transforming MIDI files into structured sequences and 2D piano-roll representations, we train and compare **LSTM** and **CNN** models to classify compositions among four legendary composers: **Bach, Beethoven, Chopin, and Mozart**.

## Objectives
* Extract temporal and structural musical features (notes, chords, tempo) from MIDI files.
* Implement a sequential **LSTM** network to capture the time-series nature of melodies.
* Implement a **CNN** architecture using 2D matrix representations (piano-rolls) of the scores.
* Evaluate and compare both models using Accuracy, Precision, and Recall.
* Optimize performance via hyperparameter tuning.

## Dataset
The project utilizes a filtered subset of the Kaggle [MIDI Classic Music Dataset](https://www.kaggle.com/datasets/blanderbuss/midi-classic-music), which contains 3,929 MIDI files across 175 composers. 
For this scope, the data is restricted to:
* Johann Sebastian Bach
* Ludwig van Beethoven
* Frédéric Chopin
* Wolfgang Amadeus Mozart

---

## Methodology & Pipeline

1. **Data Collection & Filtering:** Extracting folders belonging to the 4 target composers.
2. **Data Pre-processing & Augmentation:** Parsing MIDI formats using specialized toolkits and splitting long compositions into uniform segments.
3. **Feature Extraction:** * **For LSTM:** Encoding notes and chords into integer/one-hot event sequences.
   * **For CNN:** Converting MIDI sequences into 2D piano-roll image matrices.
4. **Model Architecture:** Training a sequence-focused LSTM and a spatial-feature-focused CNN.
5. **Evaluation:** Analyzing performance using classification reports and confusion matrices.

---

## 🗂️ Repository Structure
```text
├── .gitignore               # Excludes datasets, virtual environments, and model weights
├── README.md                # Project documentation
├── requirements.txt         # Required Python packages
├── notebooks/
│   └── composer_classification.ipynb  # Primary source code notebook
└── deliverables/
    ├── Project_Report-TeamX.pdf       # APA 7 formatted technical report
    └── Project_Notebook-TeamX.html    # Exported notebook deliverable
