Fraud Detection Using Anomaly Detection
Overview

This project aims to detect fraudulent financial transactions using anomaly detection. Because fraud cases are rare and labeled data is limited, unsupervised methods work better than traditional supervised learning. Labels were only used later to evaluate and tune the models.

Models Used

We tested four anomaly detection models:

SVM

Isolation Forest

Gaussian Anomaly Detector (PDF-based)

Autoencoder

Models were evaluated mainly with the F2-Score to prioritize recall, which is important for catching as many fraud cases as possible.

Preprocessing and Tuning

Dimensionality reduction was applied to remove noise and simplify the dataset.
We also tuned hyperparameters—especially the anomaly threshold—to find the setting that gave the best F2-Score.

To test generalization, we removed all fraud examples from the test set, allowing us to see how well the models detect unseen fraud.

Results (Test Set)

F2-Score: 0.8521

F1-Score: 0.8024

Precision: 0.7546

Recall: 0.8565

Accuracy: 0.9965

The Gaussian Anomaly Detector performed the best, offering strong recall and overall reliability in spotting fraudulent transactions.

Future Improvements

Real-time fraud detection

Ensemble methods for better performance

Adding model explainability with tools like SHAP or LIME