GENERATED AUTOMATICALLY WITH GITHUB COPILOT

# Publication Model Classifier

A machine learning system that classifies scientific publications by matching them to appropriate NASA models: ECCO, RAPID, ISSM, CMS-Flux, CARDAMOM, and MOMO-CHEM.

## Overview

This classifier uses a combination of NLP techniques to identify which scientific model a publication is associated with:

- Deep learning classification models for research areas, science keywords, and divisions
- Semantic matching using sentence transformers
- Fuzzy keyword matching with context validation
- Data-driven model affinities for different scientific domains

The system provides confidence scores with model-specific thresholds and detailed visualizations for performance analysis.

## Features

- Multi-model classification with confidence scores
- Research area, science keyword, and division classification
- Context validation against known model profiles
- Data-driven affinity analysis
- Comprehensive evaluation metrics including F1 scores, MCC, and calibration

## Requirements

- Python 3.8+
- PyTorch 1.8+
- Transformers
- SentenceTransformers
- spaCy (with en_core_web_lg model)
- scikit-learn
- RapidFuzz
- NumPy
- Matplotlib

## Getting Started

1. Install dependencies:
   ```
   pip install torch transformers sentence-transformers spacy scikit-learn rapidfuzz numpy matplotlib
   python -m spacy download en_core_web_lg
   ```

2. Download required data files:
   - curated_publications.json: Ground truth publication-model mappings
   - model_keywords.json: Model-specific keywords
   - model_descriptions.json: Model descriptions

3. Run the classifier:
   ```
   python pubclassifier.ipynb
   ```

## Evaluation

The system includes comprehensive evaluation tools:

- Performance metrics (precision, recall, F1 score, MCC)
- Threshold optimization
- Generalization analysis (train/test split, cross-validation)
- Robustness assessment
- Visualization of all metrics

## Models

The classifier works with the following NASA models:

- **ECCO**: Estimating the Circulation and Climate of the Ocean
- **RAPID**: Routing Application for Parallel Computation of Discharge
- **ISSM**: Ice-sheet and Sea-level System Model
- **CMS-Flux**: Carbon Monitoring System Flux
- **CARDAMOM**: CARbon Data MOdel fraMework
- **MOMO-CHEM**: Multi-Model Multi-Constituent Chemical...

## License

Open source for scientific research purposes.