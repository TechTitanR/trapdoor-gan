# 🔐 TrapdoorGAN: A Novel One-Way GAN for Image Encryption and Security

TrapdoorGAN is a generative adversarial network (GAN) architecture designed for **image generation with embedded secret trapdoors** — enabling secure image encryption, watermarking, and deepfake detection through bitwise trapdoor recovery.

This project demonstrates how GANs can be extended to incorporate **hidden yet recoverable patterns** for robust image security, while maintaining high-quality outputs.

---

## 📌 Key Features

- ✅ One-way image generation with embedded trapdoors
- 🧠 CNN-based trapdoor classifier for accurate bit recovery
- 🔁 Spatially redundant trapdoor embedding
- 🛡️ Adversarial training with noise/compression robustness
- 📊 Loss visualization and model evaluation metrics
- 🔒 Focus on privacy-preserving and watermarking applications

---

## 📁 Project Structure

```bash
trapdoor-gan/
├── models/               # Generator, Discriminator, Classifier architectures
├── utils/                # Dataloader, embedding logic, evaluation tools
├── train.py              # Training script for GAN + classifier
├── test.py               # Trapdoor recovery evaluation
├── config.py             # Hyperparameters and paths
├── results/              # Generated images and recovery metrics
├── checkpoints/          # Saved model weights
├── trapdoorgan-model.ipynb   # Original research notebook (for reference)
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Installation
Clone the repository and set up the environment:

```bash
git clone https://github.com/TechTitanR/trapdoor-gan.git
cd trapdoor-gan
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

---

## 🚀 Usage
🔧 Training

```bash
python train.py
```

This trains:

- A Generator to embed trapdoor bits
- A Discriminator to distinguish real vs fake images
- A CNN-based Classifier to recover trapdoor bits

---

## 📈 Evaluation
```bash
python test.py
```

This evaluates:
- Trapdoor bit recovery accuracy
- Sample images with predictions

---

## 🔍 Dataset
✅ Default: CelebA Dataset
💡 You can modify config.py to switch datasets or paths

---

## 📚 Methodology
The Generator accepts both a noise vector and a binary trapdoor bit vector. The trapdoor is spatially embedded in redundant image regions. A CNN classifier is trained alongside to predict the trapdoor bits from generated images, ensuring accurate decoding.

Additional training stability techniques include:
- Label smoothing
- Gradient clipping
- Discriminator noise
- Weighted trapdoor loss

---
## 📬 Contact
🔗 GitHub: https://github.com/TechTitanR

🏫 Institution: Manipal University Jaipur

📧 Email: rishibakliwaljain@gmail.com

---

## 🧠 Credits
Built using:

- PyTorch
- CelebA Dataset
- Matplotlib, NumPy, Pandas

Designed as part of a Minor Project on "Image Security using GANs."

