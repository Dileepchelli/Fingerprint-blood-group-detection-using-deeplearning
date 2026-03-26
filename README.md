# 🧬 Fingerprint Blood Group Detection using Deep Learning

A deep learning-based system that predicts a person’s blood group using fingerprint images, aiming to provide a non-invasive alternative to traditional blood testing.

> ⚠️ This is a research/prototype project, not a medically approved system.

---

## 🚀 Overview

Traditional blood group detection requires blood samples, lab infrastructure, and time.  
This project explores an alternative approach using fingerprint biometrics and deep learning.

The system analyzes fingerprint patterns and predicts one of the 8 blood groups.

---

## 🧠 How It Works

### Workflow

1. Input  
   - Upload fingerprint image  
   - OR scan using R307S sensor  

2. Preprocessing  
   - Grayscale conversion  
   - Resize (128×128)  
   - Noise reduction & normalization  

3. Feature Extraction  
   - CNN → extracts ridge patterns  
   - GNN → learns structural relationships  

4. Prediction  
   - Combined output → blood group classification  

---

## 🖥️ UI Preview

> 📌 Add your screenshots inside a folder like `/screenshots/` in your repo

### 🔹 Main Interface
![UI](screenshots/ui.png)

### 🔹 Upload Fingerprint
![Upload](screenshots/upload.png)

### 🔹 Prediction Output
![Output](screenshots/output.png)

### 🔹 Live Scan Result
![Live](screenshots/live.png)

---

## 🏗️ Model Architecture

- CNN (Convolutional Neural Network)  
  Extracts spatial features like ridges and textures  

- GNN (Graph Neural Network)  
  Captures fingerprint topology and connectivity  

- Final Output  

```python
final_prediction = softmax((CNN_output + GNN_output) / 2)
