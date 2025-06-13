
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

This project uses three publicly available COVID-19 chest X-ray datasets:

1. **[COVID-19 Radiography Database](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database)**  
   - Hosted on Kaggle  
   - Contains images for COVID-19, Viral Pneumonia, and Normal classes  
   - Resolution: 1024 × 1024

2. **[COVID Chest X-ray Dataset](https://github.com/ieee8023/covid-chestxray-dataset)**  
   - Maintained by Joseph Paul Cohen  
   - Includes chest X-ray and CT scans from various sources  
   - Often used in combination with RSNA pneumonia datasets

3. **[COVIDx Dataset (used in COVID-Net)](https://github.com/lindawangg/COVID-Net/blob/master/docs/COVIDx.md)**  
   - Created by aggregating several open-source datasets  
   - Large and widely used for benchmarking deep learning models

> ⚠️ Each dataset must be downloaded manually from the respective links and placed in the correct folder structure as described in the project setup.

---

---

## 📊 Results Summary

| Model + Strategy     | Dataset | Accuracy (%) | F1 Score (%) | AUC (%) |
|----------------------|---------|--------------|--------------|---------|
| CheXNet + WCL        | 1       | 98.87        | 98.21        | 99.15   |
| DenseNet201 + SMOTE  | 1       | 98.64        | 98.63        | 98.97   |
| VGG19 + WCL          | 3       | 94.87        | 94.87        | 94.86   |

> For full metrics (Sensitivity, Specificity, Precision, NPV).

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
## 📬 Contact

If you have any questions or suggestions, feel free to reach out:

**Ekram Chamseddine**  
📧 ekram.chamseddine@gmail.com
