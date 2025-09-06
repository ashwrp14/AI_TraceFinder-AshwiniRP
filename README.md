# 🧠 AI TraceFinder — Scanner Identification by Ashwini R P

This project presents a forensic-grade pipeline for identifying the source scanner of a document image using both handcrafted features and deep learning. It includes preprocessing, feature extraction, CNN training with k-fold validation, explainability, and deployment via Gradio.

---

## 📂 Project Structure

- `flatfield_features/` → Preprocessed dataset with flat-field correction  
- `official_features/` → Features extracted from the official dataset  
- `wikipedia_features/` → Features extracted from the Wikipedia dataset  
- `notebooks/` → Jupyter notebooks (.ipynb) containing preprocessing and feature extraction steps  

---

## ⚙️ Methods Used

- Grayscale Conversion  
- Wavelet Transform  
- FFT (Fast Fourier Transform)  
- PRNU (Photo-Response Non-Uniformity) Extraction  
- Feature Engineering for classification  
- CNN-based feature extraction and modeling  
- Grad-CAM for explainability  

---

## 📌 End-to-End Workflow

### 1. Data Collection & Labeling
- Manually scanned document samples using multiple scanner models (3–5 brands)
- Assigned labels based on source device metadata

### 2. Image Preprocessing
- Resized images to uniform dimensions
- Applied denoising and grayscale conversion (if needed)
- Normalized pixel values and removed non-artifact content

### 3. Feature Extraction
- Extracted noise patterns using wavelet filters and FFT
- Computed PRNU signatures, texture descriptors (LBP), and edge maps

### 4. Model Training
- Trained a **Convolutional Neural Network (CNN)** on raw PRNU images
- Applied **k-fold cross-validation** to ensure robustness (typically k=5)
- Used image augmentation (brightness, rotation) for generalization
- Tracked training metrics (accuracy, loss) across folds

### 5. Explainability
- Applied **Grad-CAM** to visualize scanner-specific activation regions
- Interpreted model decisions and feature importance

### 6. Output System
- Upload scanned image → return predicted scanner model
- Display confidence score and Grad-CAM overlay

---

## 📅 Week-wise Milestone Implementation

### 🔹 Milestone 1: Dataset Collection & Preprocessing

**Week 1**
- Collected samples from multiple scanners
- Created labeled dataset with metadata
- Analyzed image properties (resolution, format, color channels)

**Week 2**
- Resized and normalized all images
- Applied grayscale conversion and optional denoising
- Structured dataset for training

---

### 🔹 Milestone 2: Feature Engineering & Baseline Modeling

**Week 3**
- Extracted handcrafted features:
  - Noise maps
  - FFT-based frequency features
  - LBP texture descriptors
- Visualized scanner-specific patterns

**Week 4**
- Trained baseline models: Logistic Regression, SVM, Random Forest
- Evaluated using accuracy and confusion matrix
- Logged performance and limitations

---

### 🔹 Milestone 3: Deep Learning + Explainability

**Week 5**
- Built and trained CNN on raw images
- Applied data augmentation (brightness, rotation)
- Tuned hyperparameters and tracked training curves

**Week 6**
- Evaluated CNN performance (accuracy, F1-score)
- Applied Grad-CAM for model interpretability

---

### 🔹 Milestone 4: Deployment & Final Report

**Week 7**
- Built frontend UI using Gradio
- Enabled image upload and live prediction
- Logged predictions and enabled result download

**Week 8**
- Finalized documentation and system architecture
- Added training results, model comparisons, and screenshots
- Prepared presentation slides and demo walkthrough

---

## 📈 Evaluation Criteria

### ✅ Completion of Tasks
- Dataset collected and labeled correctly
- Feature engineering and modeling completed
- UI integration and testing done

### ✅ Model Quality
- CNN trained with k-fold validation
- Classification accuracy >85%
- Distinguishes between 3–5 scanner models
- Robust to image format and resolution changes

### ✅ Documentation & Demo
- Clear methodology explanation
- Performance charts (accuracy, confusion matrix)
- Explainability insights (Grad-CAM overlays)

---

## 📊 Results

The results generated from this project are stored in Google Drive:

- [Flatfield Features](https://drive.google.com/drive/folders/14e0Ml48Vd6fgq56vAN9NvJeL0pDNhzFX?usp=drive_link)  
- [Official Features](https://drive.google.com/drive/folders/1Uetwek92qsx7T3mlNe6DteDyBZh631FP?usp=drive_link)  
- [Wikipedia Features](https://drive.google.com/drive/folders/1PAUDTxNcrMMimqn9dWtddJ9NJCYqKRDX?usp=drive_link)  
- [models](https://drive.google.com/drive/folders/1m1KiKg_51F_MWVVwMDUtiXgbANx8JtCi?usp=drive_link)

---

## 📂 Datasets

The datasets used in this project are stored in Google Drive:

- [Flatfield Dataset](https://drive.google.com/drive/folders/11k9GJLxh8Jc-CkBvwuHS7vlFnTIp4h5d?usp=drive_link)  
- [Official Dataset](https://drive.google.com/drive/folders/19gP5nYPHLFrrqmWCQ3QmUyKyL_rAOiNp?usp=drive_link)  
- [Tampered Images](https://drive.google.com/drive/folders/1hZqtN8zk6sXQY_C_pCvahxNFOtoDXSpo?usp=drive_link)  
- [Wikipedia Dataset](https://drive.google.com/drive/folders/18nko4wDnxcqOPLSPIqtxaj3EE9sAHbaJ?usp=drive_link)  

---

## 🚀 Live Demo

🔗 [ScannerIdentifier App on Hugging Face Spaces](https://huggingface.co/spaces/ashwrp14/ScannerIdentifier)

Upload a PRNU image to identify the scanner model and view Grad-CAM overlays.

---

## 👩‍💻 Author

**Ashwini R P**  
GitHub: [ashwrp14](https://github.com/ashwrp14)  
Project: Infosys Virtual Forensics Initiative
