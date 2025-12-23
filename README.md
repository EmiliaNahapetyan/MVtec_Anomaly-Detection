# MVTec Anomaly Detection using Autoencoders

This project implements **unsupervised image anomaly detection** on the **MVTec AD dataset** using three reconstruction-based deep learning models:

- **AE** – Autoencoder  
- **VAE** – Variational Autoencoder  
- **MemAE** – Memory-Augmented Autoencoder  

The objective is to detect industrial defects using reconstruction error and anomaly scores, and to compare the performance of the three methods using per-class evaluation metrics.

---

## Run the Project (Google Colab)

The complete implementation is provided as a Google Colab notebook.

## Run Web App

This project can be executed directly in Google Colab.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16E9rpaDY_7iqTUR0aAxIwvCX2ZEgaQZn?usp=sharing)


Recommended: Enable GPU via  
Runtime → Change runtime type → GPU

---

## Key Features

- End-to-end anomaly detection pipeline
- Three methods: AE, VAE, and MemAE
- Training using normal images only
- Per-class AUROC evaluation
- Threshold-based classification:
  - Accuracy
  - Precision
  - Recall
  - F1-score
- Automatic checkpoint saving and reuse
- Visual demo section with reconstructions and predictions

---

## Dataset

- MVTec Anomaly Detection (MVTec AD)
- Real-world industrial inspection benchmark
- 15 object and texture classes
- Training set: normal images only
- Test set: normal and anomalous images

---

## Method Overview

All methods follow a reconstruction-based anomaly detection approach:

1. Train the model on normal images
2. Reconstruct test images
3. Compute reconstruction error as anomaly score
4. Apply anomaly thresholds
5. Evaluate performance

Models:
- AE: Standard encoder–decoder architecture
- VAE: Probabilistic latent space with KL-divergence regularization
- MemAE: Memory bank for enhanced normal pattern representation

---

## How to Use

1. Open the notebook using the Colab link
2. Run all cells sequentially
3. The dataset is downloaded automatically
4. Models are saved as checkpoints
5. Checkpoints are reused on subsequent runs

---

## Results

The notebook reports:
- Per-class AUROC scores
- Mean AUROC across classes
- Best-F1 thresholds per class
- Comparative plots for all models
- Demo visualizations with correct predictions

---

## Project Structure

This repository uses a Colab-based workflow.

- All code and experiments are contained in the notebook
- No local scripts are required
- Results are fully reproducible in Colab

---

## References

- P. Bergmann et al., MVTec AD, CVPR 2019
- D. P. Kingma and M. Welling, Auto-Encoding Variational Bayes, ICLR 2014
- I. Goodfellow et al., Deep Learning, MIT Press, 2016

---

## License

This project is intended for educational and academic use.
