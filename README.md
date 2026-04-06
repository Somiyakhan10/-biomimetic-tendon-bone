

```markdown
# 🔬 PoreScope — Automated SEM Pore Detection & Analysis

**AI-Powered Biomaterial Characterization Tool** · By Somiya Khan

[![Hugging Face](https://img.shields.io/badge/🤗-Hugging%20Face-yellow)](https://huggingface.co/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Python](https://img.shields.io/badge/Python-3.8+-green.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-red.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange.svg)

> ⚠️ **Note:** This tool is designed for research and educational purposes only. It is not intended for clinical diagnosis or regulatory decision-making.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Live Demo](#live-demo)
- [Screenshots](#screenshots)
- [Model Performance](#model-performance)
- [Dataset](#dataset)
- [How It Works](#how-it-works)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Author](#author)
- [License](#license)

---

## 🔬 Overview

**PoreScope** is an automated image analysis tool that detects and characterizes pores in Scanning Electron Microscope (SEM) images of biomaterials. It uses computer vision and machine learning to identify pore boundaries, measure pore diameters, and calculate porosity — enabling rapid, objective, and reproducible biomaterial characterization.

### Key Features

| Feature | Description |
|---------|-------------|
| 🔍 **Automated Pore Detection** | Identifies pore boundaries from SEM images |
| 📏 **Pore Diameter Estimation** | Random Forest Regression with 91% accuracy |
| 🧮 **Porosity Calculation** | Quantifies material porosity automatically |
| 📸 **Side-by-Side Visualization** | Original vs. annotated image comparison |
| 📂 **Drag-and-Drop Upload** | Easy image upload interface |
| 📊 **Exportable Results** | Table of pore metrics for further analysis |

---

## 🖥️ Live Demo

Try PoreScope live on Hugging Face Spaces:  
👉 **[Click here for live demo]** *(Add your Hugging Face Space link)*

---

## 📸 Screenshots

### Home Page
*Upload interface with drag-and-drop functionality*
<img width="1907" height="883" alt="image" src="https://github.com/user-attachments/assets/f7a5b844-c3f7-495e-99a6-549e6df695fc" />


### Analysis Results
*Side-by-side comparison: Original grayscale vs. Annotated image with detected pore boundaries*
<img width="1920" height="892" alt="image" src="https://github.com/user-attachments/assets/b3b106a6-da6b-4d9c-8cd6-dae9515f1eb5" />

### Feature Table
*Tabular results with pore metrics and calculated values*
<img width="1911" height="895" alt="image" src="https://github.com/user-attachments/assets/6f5be386-250e-43f2-b6a9-1b7155e7576f" />

---

## 📊 Model Performance

| Metric | Value |
|--------|-------|
| **Pore Detection Accuracy** | 98.6% |
| **Pore Diameter Prediction Accuracy** | 91.0% |
| **Porosity Prediction Accuracy** | 78.9% |
| **Algorithm** | Random Forest Regression |
| **Input Features** | 5 (mean, std, min, max intensity + pore count) |
| **Training Images** | 1,000 SEM images |

### Confusion Matrix (Pore Detection)

| | Detected Pore | Detected Non-Pore |
|---|---|---|
| **Actual Pore** | 98.6% | 1.4% |
| **Actual Non-Pore** | 2.1% | 97.9% |

---

## 📊 Dataset

| Property | Details |
|----------|---------|
| **Name** | SEM Images of Nanoscale Features |
| **Source** | Kaggle |
| **Total Images** | 18,577 SEM images |
| **Categories** | 10 material types |
| **Training Set** | 1,000 images |
| **Image Formats** | JPG, PNG, TIF |

### Material Categories

| Category |
|----------|
| Porous_Sponge |
| Fibres |
| Particles |
| Biological |
| Nanowires |
| Patterned_surface |
| Tips |
| Films_Coated_Surface |
| MEMS_devices_and_electrodes |
| Powder |

---

## ⚙️ How It Works

```
Upload SEM Image → Preprocess (Grayscale + Denoise) → Detect Pore Boundaries
                                                              ↓
Display Results ← Predict Diameter (Random Forest) ← Calculate Pore Metrics
```

**Step-by-step:**

1. **Upload** — User uploads an SEM image via drag-and-drop
2. **Preprocess** — Image is converted to grayscale and denoised
3. **Detect** — Computer vision algorithms identify pore boundaries
4. **Analyze** — Pore diameter, area, and porosity are calculated
5. **Predict** — Random Forest model refines diameter estimates
6. **Display** — Annotated image and results table are shown side-by-side

---

## 🛠️ Technology Stack

| Category | Technologies |
|----------|--------------|
| **Frontend & UI** | Gradio, HTML/CSS |
| **Image Processing** | OpenCV, scikit-image |
| **Machine Learning** | scikit-learn (Random Forest) |
| **Data Handling** | NumPy, Pandas |
| **Visualization** | Matplotlib |
| **Deployment** | Hugging Face Spaces |

---

## 💻 Installation

### Local Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/porescope.git
cd porescope

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py
```

### Dependencies

```txt
gradio>=4.0.0
opencv-python>=4.8.0
numpy>=1.24.0
pandas>=2.0.0
scikit-learn>=1.3.0
matplotlib>=3.7.0
scikit-image>=0.21.0
```

---

## 📁 Project Structure

```
porescope/
│
├── app.py                 # Main Gradio application
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
│
├── models/
│   └── random_forest.pkl  # Trained Random Forest model
│
├── utils/
│   ├── image_processing.py   # Preprocessing functions
│   └── pore_analysis.py      # Pore detection & metrics
│
├── samples/               # Sample SEM images for testing
│
└── assets/
    └── screenshots/       # UI screenshots for README
```

---

## 👩‍🔬 Author

**Somiya Khan**  
Biomedical Engineer | AI Researcher


---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Dataset:** SEM Images of Nanoscale Features (Kaggle)
- **Deployment:** Hugging Face Spaces 🤗
- **Libraries:** OpenCV, scikit-learn, Gradio

---

## 📬 Contact

For questions, suggestions, or collaborations, feel free to reach out!

---

*Made with ❤️ for biomaterials research and reproducible science*
```

---


---
