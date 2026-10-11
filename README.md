# CIFAR-10 Few-Shot Learning and Robustness

## Overview
This project explores image classification using a lightweight Inception-style CNN trained on a small subset of CIFAR-10. It evaluates model performance on clean and corrupted images and investigates data augmentation, regularization, error analysis, and Test-Time Augmentation (TTA).

## Dataset
- **Dataset:** CIFAR-10 (10 classes)
- **Training:** 400 images (40 per class)
- **Validation:** 100 images (10 per class)
- **Clean test:** 10,000 images
- **Shifted test:** 10,000 corrupted images

## Model
A lightweight CNN with parallel 1×1, 3×3, and 5×5 convolution branches was implemented without pretrained weights. The model follows the assignment's limit of fewer than one million parameters.

## Experiments
- **Part A:** Baseline model evaluation
- **Part B:** Geometric, photometric, and combined augmentation
- **Part C:** Batch Normalization, Dropout, L2 regularization, label smoothing, and learning-rate scheduling
- **Part D:** Ablation study comparing completed configurations
- **Part E:** Per-class accuracy, confusion matrix, misclassification analysis, and grayscale corruption testing
- **Part F:** Test-Time Augmentation using flipped and translated images

## Key Results
| Experiment | Key result |
|---|---:|
| Baseline clean accuracy | 36.35% |
| Baseline shifted accuracy | 16.80% |
| Photometric augmentation shifted accuracy | 21.82% |
| Part E clean accuracy | 10.86% |
| Part E mixed grayscale accuracy | 10.42% |
| Part F TTA shifted accuracy | 11.02% |

*Note: Results are from different experimental configurations. The low accuracy in later experiments indicates that further training and prediction analysis is needed.*

## Technologies
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn

## How to Run
1. Open the notebook in Kaggle or Jupyter Notebook.
2. Ensure TensorFlow and the required Python libraries are installed.
3. Load the CIFAR-10 dataset.
4. Run the notebook cells sequentially to reproduce the experiments and evaluations.

## Conclusion
Photometric augmentation improved shifted-test accuracy in the baseline experiments. However, later experiments showed near-random classification performance, highlighting the challenges of few-shot learning and the need for further model and training investigation.
