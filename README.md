# Galaxy Morphology & Quenching State Prediction

> **A machine learning pipeline for classifying galaxy morphology and star formation quenching using tabular and image-based astrophysical data.**

## Overview

This repository showcases a complete analysis pipeline built for astrophysics research applications. It compares model performance across:
- tabular catalog features
- galaxy imaging data
- combined tabular + image modalities

The goal is to determine whether integrating multiple data sources improves classification of galaxy morphology and quenching state.

### Why This Project?

- **Domain-driven modeling**: Applies machine learning to real astronomy data.
- **Multi-modal analysis**: Compares tabular models, image-based models, and fused approaches.
- **Practical workflows**: Demonstrates feature engineering, model evaluation, and performance comparison for classification problems.

### Objectives

This project focuses on:
- **Galaxy morphology classification**: Distinguish galaxies by structural type.
- **Quenching state prediction**: Identify galaxies transitioning from star-forming to quenched.
- **Model benchmarking**: Evaluate classic ML and deep learning methods.
- **Pipeline comparison**: Assess tabular, image, and combined model strategies.

---

## Key Features

### Multi-Modal Data Exploration

The project uses both:
- **Tabular data** from galaxy catalogs and measurements
- **Image data** from galaxy observations

This enables evaluation of how visual information complements astrophysical metadata.

### Modeling Approaches

Built and compared models including:
- Decision Trees
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Multi-Layer Perceptrons (MLP)
- Convolutional Neural Networks (CNN)

### Performance Evaluation

Focused on metrics and comparisons such as:
- Accuracy and classification performance
- Model generalization across data modalities
- Visual analysis of prediction behavior

### Data Visualizations

This repository supports:
- distribution and class balance charts
- model comparison summaries
- exploratory data plots for galaxy features

---

## Tech Stack

**Language:**
- Python 3.8+

**Core Libraries:**
- `pandas` – data manipulation
- `numpy` – numerical computing
- `scikit-learn` – classical machine learning
- `tensorflow` / `keras` or similar frameworks for CNN modeling
- `matplotlib` & `seaborn` – visualization
- `astropy` / astronomy libraries for domain-specific data handling
---

## Dataset Information

### Data Pipeline

```
Load data → Clean & preprocess → Train models → Evaluate results → Compare modalities
```

### Dataset Origin

This project combines publicly released Galaxy Zoo morphology labels with SDSS image data.

- `gz_hubble_faded.csv` is based on the **Galaxy Zoo: Hubble** faded galaxy sample. It contains morphological classifications for galaxies from Hubble Space Telescope imaging in the COSMOS field.
- The tabular labels are derived from **Galaxy Zoo 2** consensus morphology data, which is publicly available from the Galaxy Zoo data release. The dataset includes vote fractions, debiased morphology estimates, and derived class labels.
- The image data is sourced from the **SDSS / NERSC self-supervised learning release**, using 5-band SDSS photometric cutouts (ugriz) at 107x107 pixels.

### Reference Links

- Galaxy Zoo data release: https://data.galaxyzoo.org/#section-7
- SDSS/NERSC image dataset: https://portal.nersc.gov/project/dasrepo/self-supervised-learning-sdss/dataset.html


## Machine Learning Workflow

### 1. Data Preparation

- Load galaxy catalog features and observational data
- Clean missing values and normalize features
- Create training and test splits for evaluation

### 2. Model Training

- Train multiple classifiers on tabular data
- Train CNN models on galaxy image data
- Compare combined approaches when both data modalities are available

### 3. Evaluation Metrics

Models are evaluated using:
- Accuracy
- Precision, recall and F1-score
- Model comparison across notebooks

---

## Results & Findings

### Key Observations

- **Tabular models** provide strong baseline performance using catalog features.
- **CNN-based image models** capture morphological patterns directly from galaxy images.
- **Combined modeling** offers a clear pathway to improving classification by integrating multiple data sources.

### Model Comparison Highlights

- Decision Tree, KNN, Naive Bayes, and MLP models are benchmarked on tabular datasets.
- CNN architectures are evaluated for image-based morphology classification.
- The analysis highlights where each approach is most effective.

---

## Quick Start

### Prerequisites
- Python 3.8+
- `pip` or `conda`

### Installation

Clone the repository:
```bash
git clone https://github.com/Janya22/galaxy-morphology-quenching-ml.git
cd galaxy-morphology-quenching-ml
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Run the notebooks:
```bash
jupyter notebook tabular_preprocessing.ipynb
jupyter notebook MLP.ipynb
jupyter notebook CNN.ipynb
```

---

## Project Structure

```
├── README.md
├── CNN.ipynb
├── DecisionTree.ipynb
├── KNN.ipynb
├── MLP.ipynb
├── NaiveBayes.ipynb
├── MLP_morphology_classification.ipynb
├── tabular_preprocessing.ipynb
├── image_preprocessing.ipynb
└── gz_hubble_faded.csv

```

---

## Team

| Contributor |
|-------------|
| **Adam Aboushady** |
| **Ihsan Fazal** |
| **Janya Rathnakumar** |
| **Mustansir Eranpurwala** |
| **Vaishnavi Chintha** |

---

## License

This repository is intended for **portfolio and professional demonstration purposes**.
