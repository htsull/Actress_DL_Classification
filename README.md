# 🧠 Doppelganger Face Classification Model Experiment

This repository contains experiments for classifying images of actresses using convolutional neural networks (CNNs) with PyTorch. The goal is to discriminate between three classes:

- 🎭 **Natalie Portman**
- 🎭 **Keira Knightley**
- 🧍 **Others**

The two first classes were chosen because the actresses are commonly mistaken for each other. A small dataset of cropped portrait images is provided to train and evaluate the models.

---

## 📁 Dataset

The `data` directory is organized as follows:

```
data/
├── train/  (429 images)
└── val/    (168 images)
```

Both `train` and `val` contain the three sub‑folders `Natalie`, `Kiera` and `Autres` with images of size 530×400 pixels.

---

## 🚀 Approach

The project explores two main strategies:

1. 🧪 **Training custom CNN models.** Several network configurations were tested by varying the number of convolutional layers and pooling operations. Images are normalized and augmented before training.
2. 🧠 **Transfer learning.** Pre‑trained architectures such as EfficientNet (b0–b7), ResNet18, ResNet152 and Inception v3 are fine‑tuned on the dataset.

🔧 The best result with a custom architecture was achieved with the configuration:


```
config0 = [64, "M", 256, "M", 512, "M"]
```

- ✅ Training accuracy: **55.7%**
- 📉 Validation accuracy: **40.5%**

Using transfer learning with **ResNet18** improved the validation accuracy to **60.7%**. 📈

---

## 📦 Repository Contents

- 📓 `classProject.ipynb` – main notebook used to run the experiments.
- 🧪 `Trash - Tests/` – additional exploratory notebooks.
- 💾 `checkpoint/ckpt.t7` – example of a saved model checkpoint.

---

## 🛠️ Getting Started

Open `classProject.ipynb` with Jupyter or Google Colab to reproduce the experiments. The notebook expects the image folders to be available under `data/train` and `data/val` as shown above.
