# 📄 Forensic Scanner Identification Toolkit

This repository contains all components of the forensic scanner identification pipeline, including feature sets, trained models, scalers, encoders, residuals, and prediction logs. It supports hybrid, stacked, SVM, RF, and LGBM classifiers, with tampering detection and confidence scoring.

---
##Scanner 

- [ScannerApp (Google Drive)](https://drive.google.com/drive/folders/1QKZCHqIDAZaLWt5K9HlM8ODncRH_h7kz?usp=drive_link)
## 🔍 Feature Sets

| File | Description |
|------|-------------|
| [Enhanced Features](https://drive.google.com/file/d/12TiibMIlHKazECSYgJWxwa7hVcgSSMjt/view?usp=drive_link) | Final enhanced feature matrix |
| [Raw Features](https://drive.google.com/file/d/1w44DYWJQ14Jl97UmUA8FW2v6yGxERFWr/view?usp=drive_link) | Original extracted features |
| [Flatfield Residuals](https://drive.google.com/file/d/1O-rs0iDSDvFzZS4G-zoX1OHSd3MA4Kk1/view?usp=drive_link) | Residuals from flatfield correction |
| [Official Wiki Residuals](https://drive.google.com/file/d/1kGOZzX1Yzwrdh_ZEYNv62rE7YcZgoLCX/view?usp=drive_link) | Residuals from official scanner dataset |

---

## ⚙️ Hybrid Model Components

| File | Description |
|------|-------------|
| [Hybrid Feature Scaler](https://drive.google.com/file/d/1tnwypdYUQ7kaY9Aa22lLeINyK5JczpEa/view?usp=drive_link) | Scaler used for hybrid model |
| [Hybrid Label Encoder](https://drive.google.com/file/d/1ExoUzdLmi50P45WZZjT_KzFMoM99bWZY/view?usp=drive_link) | Label encoder for hybrid classes |
| [Hybrid Training History](https://drive.google.com/file/d/1rINEafNFmhAkqRkz4pTC3QlOwIujp41Z/view?usp=drive_link) | Training metrics and loss curves |
| [Hybrid Model (.keras)](https://drive.google.com/file/d/1P1OFs39ymmxBjfK4SkmBtmwojxlv6FL6/view?usp=drive_link) | Intermediate hybrid model |
| [Hybrid Final Model (.keras)](https://drive.google.com/file/d/1TMi9q3ja9RuxU9fKLR4g3OEEKH2T2bli/view?usp=drive_link) | Final hybrid model with tampering detection |

---

## 🌲 Random Forest (RF) Components

| File | Description |
|------|-------------|
| [RF Label Encoder](https://drive.google.com/file/d/1J033xeRZI8TjUfx8LEtnpMpX8r0Qx7ys/view?usp=drive_link) | Label encoder for RF model |
| [RF Scaler](https://drive.google.com/file/d/1JbUvCYb7Jg0-XS4Nw4dGz7WbbcKgcquu/view?usp=drive_link) | Feature scaler for RF |
| [RF Model](https://drive.google.com/file/d/1GnBNkwwOteWi-gw_Vl43H3CJMZpOj3kb/view?usp=drive_link) | Trained RF model |

---

## 🌟 LightGBM (LGBM) Components

| File | Description |
|------|-------------|
| [LGBM Label Encoder](https://drive.google.com/file/d/1gfpf2xaV7wgYmL0kWX6VJXzkqOwlivK0/view?usp=drive_link) | Label encoder for LGBM |
| [LGBM Scaler](https://drive.google.com/file/d/15nfPiRy_cwPDU4nNu-WzvGHB55woNEX_/view?usp=drive_link) | Scaler for LGBM |
| [LGBM Model](https://drive.google.com/file/d/1j0WKMY0jarEqzxaRsKDRrS_snjU5kIHT/view?usp=drive_link) | Trained LGBM model |

---

## 🧠 Stacked Model Components

| File | Description |
|------|-------------|
| [Stacked Label Encoder](https://drive.google.com/file/d/1RbJwl5qkJ53LCZK0KO8pyQm6_e5k209c/view?usp=drive_link) | Label encoder for stacked model |
| [Stacked Scaler](https://drive.google.com/file/d/1U0ayV0SltCt4rDUd9dvdoLILOe0LEz7M/view?usp=drive_link) | Scaler for stacked model |
| [Stacked Model](https://drive.google.com/file/d/1GOyfueK8nyk9_qUFqtAV8l_WYbCHDSHn/view?usp=drive_link) | Final stacked classifier |

---

## 💻 SVM Model Components

| File | Description |
|------|-------------|
| [SVM Label Encoder](https://drive.google.com/file/d/1Xqi-Cv69QZTc-IRdYCXa-EEeqWP8iVa_/view?usp=drive_link) | Label encoder for SVM |
| [SVM Scaler](https://drive.google.com/file/d/1Dk3FLQI2ap4pU2Pi0vMbhdnQ7psv_cmf/view?usp=drive_link) | Scaler for SVM |
| [SVM Model](https://drive.google.com/file/d/1vSF6KainfQZb1Pxs7LJTmw5Vbu3KX8NO/view?usp=drive_link) | Trained SVM model |

---

## 📊 Prediction Logs

| File | Description |
|------|-------------|
| [Prediction Log CSV](https://drive.google.com/file/d/15U_RGPIKUHyBSH-3A-ohZB2vleMzR56x/view?usp=drive_link) | Batch predictions with confidence scores |

---

## ✍️ Author

Developed and curated by **Ashwini**, with a focus on forensic-grade accuracy, modular deployment, and public usability.  
For questions, collaborations, or citations, please credit: `Ashwini | Forensic Scanner Identification Toolkit`.

---

## 🚀 Deployment Notes

- All models are compatible with `Gradio`, `Streamlit`, and `Flask` interfaces.
- Ensure matching encoders and scalers are used during inference.
- Tampering warnings and confidence scores are integrated in the hybrid pipeline.
- For Hugging Face Spaces, include `requirements.txt`, `app.py`, and this `README.md`.

---




