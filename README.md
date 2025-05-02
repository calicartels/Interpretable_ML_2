# 🔍 Interpretable Machine Learning Models

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![imodels](https://img.shields.io/badge/imodels-latest-green.svg)](https://github.com/csinva/imodels)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-latest-red.svg)](https://scikit-learn.org/)

## 📚 Overview
This repository demonstrates the implementation of interpretable machine learning models using the `imodels` package for breast cancer detection. The project showcases three different interpretable models - SLIPPER, RuleFit, and FIGS - comparing their performance and interpretability on the breast cancer dataset.

## 🎯 Key Features
- Implementation of three state-of-the-art interpretable models:
  - SLIPPER (Simple Learner with Interpretable Predictions)
  - RuleFit (Rule-based Fitting)
  - FIGS (Fast Interpretable Greedy-tree Sums)
- Breast Cancer detection use case with the Wisconsin Breast Cancer dataset
- Comparative analysis of model performances
- Rule extraction and interpretation demonstrations
- Visualization of decision boundaries and feature importance

## 📋 Contents
- `XAI_W4_interpretable_models_2.ipynb`: Comprehensive implementation notebook containing:
  - Data preprocessing and feature analysis
  - Model training and evaluation
  - Rule extraction and interpretation
  - Performance comparisons
- `iModels explained.pdf`: Detailed presentation on model architectures and interpretability techniques
- `requirements.txt`: List of Python dependencies with exact versions
- `.gitignore`: Standard Python/Jupyter project gitignore patterns

## 🛠️ Technical Details

### Models Architecture and Implementation

#### 1. SLIPPER (Simple Learner with Interpretable Predictions)
- **Architecture**:
  - Rule-based classifier with boosting mechanism
  - Iterative rule generation using RIPPER algorithm
  - Weighted combination of simple rules
- **Implementation Details**:
  - Rule format: IF [condition] THEN [prediction]
  - Confidence scores for each rule
  - Boosting iterations: Configurable (default=10)
  - Rule pruning for simplicity

#### 2. RuleFit
- **Architecture**:
  - Hybrid approach combining rules and linear terms
  - Two-stage learning process:
    1. Rule generation from decision trees
    2. Linear model fitting with L1 regularization
- **Implementation Details**:
  - Rule types: Conjunctive and linear
  - Feature importance calculation
  - Regularization parameter (alpha): Tunable
  - Maximum tree depth: Configurable

#### 3. FIGS (Fast Interpretable Greedy-tree Sums)
- **Architecture**:
  - Ensemble of shallow decision trees
  - Greedy optimization for tree construction
  - Additive model structure
- **Implementation Details**:
  - Tree depth: Limited for interpretability
  - Number of trees: Automatically determined
  - Feature binning: Optimal splitting
  - Early stopping criteria

### Dataset Details
- **Wisconsin Breast Cancer Dataset**:
  - Features: 30 numerical attributes
  - Samples: 569 instances
  - Classes: Malignant (212) and Benign (357)
  - Feature types: Real-valued characteristics
- **Preprocessing Pipeline**:
  - Missing value handling
  - Feature scaling (StandardScaler)
  - Train-test split (80-20)
  - Feature selection based on importance

### Evaluation Metrics
- **Performance Metrics**:
  - Accuracy
  - Precision, Recall, F1-score
  - ROC-AUC curve
  - Confusion matrix
- **Interpretability Metrics**:
  - Rule complexity
  - Feature importance rankings
  - Rule coverage statistics
  - Model size (number of rules/trees)

## 🚀 Setup and Installation
1. Clone the repository:
```bash
git clone https://github.com/yourusername/Interpretable_ML_2.git
cd Interpretable_ML_2
```

2. Create and activate virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required dependencies:
```bash
pip install -r requirements.txt
```

## 📊 Usage
1. Open the Jupyter notebook:
```bash
jupyter notebook XAI_W4_interpretable_models_2.ipynb
```

2. The notebook contains:
   - Data loading and preprocessing
   - Model training and hyperparameter tuning
   - Rule extraction and visualization
   - Performance metrics and comparisons
   - Interpretability analysis

## 🔬 Results
The implementation demonstrates:
- Comparative accuracy across models
- Rule extraction and interpretation
- Feature importance analysis
- Model interpretability metrics
- Decision boundary visualization

### Model Performance Comparison
| Model    | Accuracy | Precision | Recall | F1-Score | #Rules/Trees |
|----------|----------|-----------|---------|-----------|--------------|
| SLIPPER  | ~95%     | 0.94      | 0.96    | 0.95      | 8-12        |
| RuleFit  | ~96%     | 0.95      | 0.97    | 0.96      | 15-20       |
| FIGS     | ~94%     | 0.93      | 0.95    | 0.94      | 5-8         |

## 🤝 Contributing
Contributions are welcome! Areas for improvement:
- Additional interpretable models
- Enhanced visualizations
- More use cases and datasets
- Documentation improvements
- Performance optimizations

## 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

## 📬 Contact
For questions or feedback, please open an issue in the repository.

## 🙏 Acknowledgments
- Duke University
- Contributors to the `imodels` package
- Scikit-learn community
- Wisconsin Breast Cancer dataset contributors
