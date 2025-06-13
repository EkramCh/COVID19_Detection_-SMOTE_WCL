
# 🩺 COVID-19 Chest X-Ray Classification with SMOTE and Weighted Loss

This repository contains the official implementation of the paper:

> **"Handling class imbalance in COVID-19 chest X-ray images classification: Using SMOTE and weighted loss"**  
> 📄 *Ekram Chamseddine, Nesrine Mansouri, Makram Soui, Mourad Abed*  
> Published in *Applied Soft Computing, Elsevier, 2022*  
> [🔗 DOI: 10.1016/j.asoc.2022.109588](https://doi.org/10.1016/j.asoc.2022.109588)

---

## 📌 Overview

This project presents a deep learning pipeline for **multiclass classification** of chest X-ray (CXR) images to detect:

- 🦠 COVID-19
- 😷 Viral Pneumonia
- ✅ Normal (Healthy)

To overcome the **class imbalance** typically found in medical datasets, we apply two powerful strategies:

- **SMOTE (Synthetic Minority Over-sampling Technique)**
- **Weighted Categorical Cross-Entropy Loss**

We train and evaluate six CNN architectures using **transfer learning** to identify the best-performing model.

---

## 🧠 Models

- DenseNet201
- CheXNet (DenseNet121)
- MobileNetV2
- ResNet152
- VGG19
- Xception

Each model is fine-tuned for multi-class classification using preprocessed chest X-ray datasets.

---

## 📂 Datasets

We used three public COVID-19 X-ray datasets:

1. **COVID-19 Radiography Database**  
2. **COVIDx Dataset**  
3. **COVID ChestX-ray Dataset**

Links and instructions to access them are provided in `data/README.md`.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/EkramCh/COVID19_Detection_-SMOTE_WCL.git
cd COVID19_Detection_-SMOTE_WCL
```

### 2. Install requirements

```bash
pip install -r requirements.txt
```

### 3. Prepare the data

Ensure the datasets are downloaded and stored in `data/` with the following structure:

```
data/
├── dataset1/
├── dataset2/
└── dataset3/
```

### 4. Train a model

```bash
python train.py --model DenseNet201 --dataset dataset1 --balance WCL
```

Options for `--balance`: `WCL` or `SMOTE`

### 5. Evaluate the model

```bash
python evaluate.py --weights saved_models/densenet201_wcl.h5
```

---

## 📊 Results Summary

| Model + Strategy     | Dataset | Accuracy (%) | F1 Score (%) | AUC (%) |
|----------------------|---------|--------------|--------------|---------|
| CheXNet + WCL        | 1       | 98.87        | 98.21        | 99.15   |
| DenseNet201 + SMOTE  | 1       | 98.64        | 98.63        | 98.97   |
| VGG19 + WCL          | 3       | 94.87        | 94.87        | 94.86   |

> For full metrics (Sensitivity, Specificity, Precision, NPV), refer to the paper or `results/` folder.

---

## 🏗️ Project Structure

```
├── data/               # Raw and preprocessed datasets
├── models/             # Model definitions
├── results/            # Saved results and metrics
├── train.py            # Training script
├── evaluate.py         # Evaluation script
├── utils.py            # Helper functions
├── README.md
└── requirements.txt
```

---

## 📚 Citation

If you use this repository, please cite our work:

```bibtex
@article{chamseddine2022covid,
  title={Handling class imbalance in COVID-19 chest X-ray images classification: Using SMOTE and weighted loss},
  author={Chamseddine, Ekram and Mansouri, Nesrine and Soui, Makram and Abed, Mourad},
  journal={Applied Soft Computing},
  volume={129},
  pages={109588},
  year={2022},
  publisher={Elsevier}
}
```

---

## 📬 Contact

If you have any questions or suggestions, feel free to reach out:

**Ekram Chamseddine**  
📧 ekram.chamseddine@gmail.com
