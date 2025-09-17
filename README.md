# 🧠 AI TraceFinder — Scanner Identification by Ashwini R P

This repository presents a forensic-grade pipeline for identifying the source scanner of a document image using handcrafted features and a single, robust classifier: **XGBoost**. The system includes preprocessing, feature extraction, model training and testing, explainability via Grad-CAM, and deployment via Gradio.

---

## ⚙️ Methods Used

- Grayscale Conversion  
- Wavelet Transform  
- FFT (Fast Fourier Transform)  
- PRNU (Photo-Response Non-Uniformity) Extraction  
- Feature Engineering for classification  
- XGBoost-based training and testing  
- Grad-CAM for explainability  

---

## 📌 End-to-End Workflow

1. **Data Collection & Labeling**  
   - Scanned samples from 3–5 scanner brands  
   - Labeled using device metadata  

2. **Image Preprocessing**  
   - Resized, denoised, and normalized images  
   - Removed non-artifact content  

3. **Feature Extraction**  
   - Wavelet + FFT-based noise patterns  
   - PRNU signatures, LBP textures, edge maps  

4. **Model Training (XGBoost)**  
   - Trained XGBoost classifier on extracted features  
   - Applied k-fold validation (typically k=5)  
   - Augmentation: brightness, rotation  

5. **Explainability**  
   - Grad-CAM overlays for scanner-specific regions  
   - Feature importance interpretation  

6. **Output System**  
   - Upload scanned image → predict scanner model  
   - Display confidence score + Grad-CAM overlay  

---

## 📅 Week-wise Milestones

| Week | Milestone |
|------|-----------|
| 1–2  | Dataset collection, labeling, preprocessing |
| 3–4  | Feature engineering, XGBoost modeling |
| 5–6  | Validation, Grad-CAM explainability |
| 7–8  | Gradio deployment, documentation, demo |

---

## 📈 Evaluation Criteria

✅ Task Completion  
✅ Model Accuracy (>85%)  
✅ Robustness across formats  
✅ UI Integration  
✅ Explainability (Grad-CAM)  
✅ Documentation & Demo  

---

## 📊 Results & Prediction Logs

| File | Description |
|------|-------------|
| Enhanced Features | Final enhanced feature matrix |
| Raw Features | Original extracted features |
| Flatfield Residuals | Residuals from flatfield correction |
| Official Wiki Residuals | Residuals from official scanner dataset |
| Prediction Log CSV | Batch predictions with confidence scores |

---

## 📂 Dataset Links (Google Drive)

- Flatfield Images: [Link](https://drive.google.com/file/d/1O-rs0iDSDvFzZS4G-zoX1OHSd3MA4Kk1/view?usp=drive_link)  
- Official Documents: [Link](https://drive.google.com/file/d/1kGOZzX1Yzwrdh_ZEYNv62rE7YcZgoLCX/view?usp=drive_link)  
- Tampered Images: [Link](https://drive.google.com/file/d/15U_RGPIKUHyBSH-3A-ohZB2vleMzR56x/view?usp=drive_link)  
- Wikipedia Documents: [Link](https://drive.google.com/file/d/1w44DYWJQ14Jl97UmUA8FW2v6yGxERFWr/view?usp=drive_link)  

---

## 🚀 Live Demo

🔗 [ScannerIdentifier App on Hugging Face Spaces](https://huggingface.co/spaces/ashwrp14/AI_tracer)  
Upload a PRNU image to identify the scanner model and view Grad-CAM overlays.

---

## ✍️ Author

Developed and curated by **Ashwini R P**  
GitHub: [ashwrp14](https://github.com/ashwrp14)  
Project: Infosys Virtual Forensics Initiative  

For questions, collaborations, or citations, please credit:  
**Ashwini | Forensic Scanner Identification Toolkit**

---

## 🛠️ Deployment Notes

- The model is deployed via Gradio and supports live image upload  
- Ensure feature extraction matches training format before inference  
- Confidence scores and Grad-CAM overlays are integrated  
- For Hugging Face Spaces, include `requirements.txt`, `app.py`, and this `README.md`  

---
