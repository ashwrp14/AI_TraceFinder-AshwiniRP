# Scanner Source Identification Project  

## 1. Data Collection & Labeling  
- Manually scan sample images using multiple scanners  
- Assign proper labels based on source device  

## 2. Image Preprocessing  
- Resize, denoise, convert to grayscale if needed  
- Normalize pixels and remove non-artifact content  

## 3. Feature Extraction  
- Extract noise patterns using filters (wavelet, FFT)  
- Compute PRNU, texture descriptors, edge patterns  

---

## Milestone 1: Dataset Collection & Preprocessing  

### Week 1  
- Collect scanned document samples from different scanner devices (minimum 3–5 models/brands).  
- Create a labeled dataset (e.g., scanner_model, file_name, etc.).  
- Analyze basic image properties: resolution, format, color channel, etc.  

### Week 2  
- Perform image preprocessing:  
  - Resize all images to a fixed dimension  
  - Convert to grayscale if needed  
  - Denoise (optional)  
- Normalize and structure the dataset for model training.  

---

## Milestone 2: Feature Engineering & Baseline Modeling  

### Week 3  
- Extract hand-crafted features like:  
  - Noise patterns  
  - Frequency domain features (e.g., FFT)  
