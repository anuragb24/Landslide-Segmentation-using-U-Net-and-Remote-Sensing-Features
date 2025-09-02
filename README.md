 
# Landslide Segmentation using U-Net and Remote Sensing Features

## Objective

This project develops a **deep learning framework** to automatically detect and map landslides from **multi-modal remote sensing tiles (Sentinel-1/2 + DEM features)** using semantic segmentation.

---

## Methodology

* **Dataset:** 3,799 training tiles (128×128 px, HDF5) with binary masks and 245 validation tiles.
* **Features:** Created **6-channel inputs** per tile — RGB bands, NDVI (vegetation index), slope, and elevation.
* **Preprocessing:** Normalization, NaN handling, and 80–20 train/validation split.
* **Model:** Implemented a **U-Net Convolutional Neural Network (CNN)** in TensorFlow/Keras with encoder–decoder and skip connections.
* **Training:** 100 epochs, batch size 16, Binary Cross-Entropy loss, Adam optimizer, with metrics F1-Score, Precision, Recall, and Accuracy.
* **Evaluation:** Saved the best checkpoint model based on validation F1-Score and generated predicted masks for unseen tiles.

---

## Results

* Achieved strong validation performance:

  * **F1-Score ≈ 0.82**
  * **Precision ≈ 0.80**
  * **Recall ≈ 0.84**
  * **Accuracy ≈ 0.88**
* Produced **binary segmentation masks** that can be integrated into GIS workflows for automated **landslide hazard mapping and risk assessment**.
 
