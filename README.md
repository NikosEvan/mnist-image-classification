# Image Classification using MNIST Dataset

This repository contains two indepentant studies on image classification, serving as an introduction to some foundamental machine learning algorithms. During the coursework, we encountered real-world problematic situations, vulnerabilities of classic machine learning architectures and explored optimization dynamics.

## Projects Overview

### 1. Linear Classifiers: Class Imbalance and Distribution Shifts
An in-depth evaluation of Softmax Regression and Perceptrons (OvA, OvO), implemented from scratch. 
* **Key Focus:** Optimization dynamics, capacity constraints, and the geometric collapse of decision boundaries under extreme class imbalance (20:1 ratio) and data scarcity.
* **Key Finding:** Demonstrated the "Validation Illusion" (Distribution Shift)—showing how skewed cross-validation sets heavily reward naive models and penalize cost-sensitive minority predictions. This proves that validation metrics are fundamentally invalid for model selection if a distribution shift exists between the evaluation space and the target real-world distribution.

### 2. Multimodal Classification: Dimensionality Reduction and Unsupervised Clustering
A study on dimensionality reduction, unsupervised clustering (K-Means), and distance metrics, culminating in a custom Multimodal Mahalanobis-based Classifier.
* **Key Focus:** Principal Component Analysis (PCA), K-Means++ clustering, and Mahalanobis distance.
* **Theoretical Insights:** Highlighted PCA as a strict mathematical prerequisite for computing Mahalanobis distance in high-dimensional spaces, explained the theoretical link between the Mahalanobis metric and Maximum Likelihood Estimation (MLE), and demonstrated the mathematical equivalence of L2-normalized Euclidean distance to Cosine similarity.
* **Architectural Progression:** Evolved a naive Euclidean Nearest Centroid Classifier (which assumes one spherical distribution per digit) into a robust Mahalanobis classifier that models distinct ellipsoidal distributions via class-specific covariance matrices. By utilizing K-Means to partition digits into subclasses, the final model successfully captures intra-class variance and distinct handwriting styles.
