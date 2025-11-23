# Brain-Tumor-Segmentation
# 🧠 Brain Tumor Segmentation using U-Net (BRATS2020)

Deep learning project for segmenting brain tumors from multi-modal MRI scans using a custom **U-Net architecture**, trained on the **BRATS2020 dataset** using **Kaggle GPU**.

This model performs **pixel-wise medical image segmentation** and highlights tumor regions for clinical research and diagnosis support.

---

## 🚀 Features

- Multi-modal MRI support (FLAIR, T1, T1CE, T2)
- Custom U-Net with skip connections
- Dice + Binary Cross Entropy Loss
- High performance — **99% validation accuracy (0.99 Dice Score)**
- Dataset loading, preprocessing, training & visualization integrated end-to-end

---

## 📂 Dataset

This project uses the **BRATS2020 (Brain Tumor Segmentation Challenge)** dataset.

Each MRI scan contains 4 modalities:

| Modality | Purpose |
|----------|---------|
| **FLAIR** | Edema / swelling regions |
| **T1** | Structural details |
| **T1CE** | Enhancing tumor core |
| **T2** | Fluid-affected tissue |

Dataset format: **NIfTI (.nii)** volumetric scans.

👉 Download via Kaggle: *(add your link if you imported manually)*  
> `kaggle datasets download -d ...`  

---

## 🏗 Model Architecture (U-Net)

The U-Net architecture used:

- Input: **(128 × 128 × 4)**
- Filters: **64 → 128 → 256 → 512 → 1024**
- Output: **(128 × 128 × 1), Sigmoid**
- Skip connections for spatial feature preservation

Training parameters:

| Parameter | Value |
|-----------|-------|
| Batch Size | 8 |
| Epochs | 40 |
| Optimizer | Adam (0.001) |
| Loss | Dice + BCE |
| Metric | Dice Coefficient |

---

## ⚙ Installation & Setup

### **🩻 Run Directly on Kaggle (Recommended)**

1. Open Kaggle Notebook
2. Enable GPU:  
   **Settings → Accelerator → GPU**
3. Upload or attach dataset
4. Run all cells

✔ No local setup required.

---

### **🖥 Local Setup (Optional)**

```bash
git clone https://github.com/<your-username>/brain-tumor-segmentation.git
cd brain-tumor-segmentation
pip install -r requirements.txt
Example dependencies:

txt
Copy code
tensorflow
numpy
nibabel
opencv-python
matplotlib
scikit-learn
🧪 Training
Once files are loaded:

python
Copy code
history = model.fit(X_train, y_train, batch_size=8, epochs=40, validation_data=(X_val, y_val))
📊 Results
Metric	Value
Validation Accuracy	~99%
Dice Score	0.99
Loss	Low + stable

Example output visualization:

Original MRI slice

Ground Truth Mask

Model Prediction Overlay

(Add images/screenshots here)

🧾 Folder Structure
kotlin
Copy code
📦 brain-tumor-segmentation
│── 📁 data/
│── 📁 notebooks/
│── 📁 outputs/
│── model.py
│── preprocessing.py
│── README.md
🧬 Applications
Tumor boundary detection

Radiology diagnostics assistance

Research on medical imaging segmentation

Surgical planning

🤝 Contributing
Pull requests are welcome!
If contributing major changes, please open an issue first.

📚 Citation
If you use this dataset, cite BRATS challenge papers.

BRATS: Brain Tumor Segmentation Challenge
https://www.med.upenn.edu/cbica/brats2020/

📜 License
This project is for research & educational use only
(not intended for clinical deployment without validation).

⭐ If you found this useful, give the repo a star!
markdown
Copy code

---

### **✔ Next Step**

If you want, I can also generate:

- `requirements.txt`
- `CONTRIBUTING.md`
- `model_architecture.png`
- Notebook refactor into modules
