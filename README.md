# Deep Learning for Classical Composer Identification

Using Convolutional Neural Networks (CNN) and Long Short-Term Memory (LSTM) networks to accurately identify classical music composers from MIDI files.

---
## Contributors
* **Christian Lopez**
* **Idrees Khan**
* **Lashana Narayan**

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

To facilitate seamless team collaboration without requiring local Kaggle API keys, the dataset has been securely hosted on a shared Google Drive. You can view or manually download the dataset file here: 
**[Google Drive Dataset Link - midi-classic-music.zip](https://drive.google.com/file/d/1QJPbVi6q2QPIiD47ZBf9tDxhM4ON-7mj/view?usp=share_link)**
The notebooks are configured to automatically download and extract this dataset directly into the cloud environment's temporary storage using the `gdown` library.

For this scope, the data is restricted and balanced across four targets:
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

## Libraries & Tools Used

This project relies on several key open-source libraries for data processing, music analysis, and deep learning:

* **TensorFlow / Keras:** For building, training, and evaluating the LSTM and CNN architectures.
* **pretty_midi:** For parsing, manipulating, and extracting piano-roll matrices from MIDI files.
* **music21:** For extracting musicological features (notes, chords, tempo) from the scores.
* **scikit-learn:** For data splitting (train/test split) and calculating evaluation metrics (Precision, Recall, Confusion Matrices).
* **gdown:** For securely downloading dataset zips directly from Google Drive into the cloud runtime.
* **NumPy & Pandas:** For array manipulation, sequence formatting, and structuring datasets.
* **Matplotlib / Seaborn:** For visualizing training loss/accuracy curves and confusion matrices.

---

## Repository Structure
```text
├── .gitignore               # Excludes datasets, virtual environments, and model weights
├── README.md                # Project documentation
├── requirements.txt         # Required Python packages
├── notebooks/
│   └── composer_classification.ipynb  # Primary source code notebook
└── deliverables/
    ├── Project_Report-TeamX.pdf       # APA 7 formatted technical report
    └── Project_Notebook-TeamX.html    # Exported notebook deliverable
