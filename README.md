# Tendon-Bone Interface Simulator — Biomimetic Gradient Design & Analysis

## AI-Powered Computational Platform for Mechano-Chemical Tissue Interface Simulation · By PhD Research Project

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.12+-green.svg)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-2.0.2-blue.svg)](https://numpy.org/)
[![SciPy](https://img.shields.io/badge/SciPy-1.16.3-orange.svg)](https://scipy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.10.0-red.svg)](https://matplotlib.org/)

> ⚠️ **Note**: This simulator is designed for research and educational purposes only. It is not intended for clinical diagnosis, medical device certification, or regulatory decision-making without experimental validation.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Screenshots & Visual Outputs](#-screenshots--visual-outputs)
- [Model Performance](#-model-performance)
- [Gradient Profiles](#-gradient-profiles)
- [How It Works](#-how-it-works)
- [Technology Stack](#-technology-stack)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Next Steps (Phase 2)](#-next-steps-phase-2)
- [Author](#-author)
- [License](#-license)

---

## 🧬 Tendon-Bone Interface Simulator — Biomimetic Gradient Design & Analysis

### AI-Powered Computational Platform for Mechano-Chemical Tissue Interface Simulation · By PhD Research Project

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.12+-green.svg)](https://www.python.org/)
[![NumPy](https://img.shields.io/badge/NumPy-2.0.2-blue.svg)](https://numpy.org/)
[![SciPy](https://img.shields.io/badge/SciPy-1.16.3-orange.svg)](https://scipy.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.10.0-red.svg)](https://matplotlib.org/)

> ⚠️ **Note**: This simulator is designed for research and educational purposes only. It is not intended for clinical diagnosis, medical device certification, or regulatory decision-making without experimental validation.

---

## 📸 Screenshots & Visual Outputs

### Stiffness Gradient Profiles
*Comparison of linear, sigmoidal (biomimetic), and exponential gradient designs*

| Linear Gradient | Sigmoidal Gradient | Exponential Gradient |
|----------------|-------------------|----------------------|
| *Uniform transition* | *Biomimetic S-curve* | *Rapid early stiffening* |

---

### Mechanical Analysis Dashboard

| Stress Distribution | Modulus-Stress Correlation |
<img width="1910" height="865" alt="image" src="https://github.com/user-attachments/assets/8c0c220e-a2d8-4de6-bf18-1ed4e7f38b23" />


---

### Biological Simulation

| Day 0: Initial Seeding | Day 28: Differentiated Co-culture |
|------------------------|-------------------------------------|
| *Tenocyte-rich near soft region* | *Osteoblast-rich near hard region* |

<img width="1920" height="834" alt="image" src="https://github.com/user-attachments/assets/e7367b70-9bf3-4ebb-aef5-e7c79c761d9a" />

---

### Fatigue Life Prediction

| Fatigue Life Distribution | Stiffness Degradation | Design Validation |

<img width="959" height="442" alt="image" src="https://github.com/user-attachments/assets/488948c9-db77-4d47-85ce-96f1de0a61ab" />

---

### Final Summary Dashboard

| Modulus Gradient | Stress Distribution | Day 28 Cell Distribution | Performance Radar |
|-----------------|---------------------|--------------------------|--------------------|
| *10 → 1000 MPa* | *Peak stress location* | *Tenocyte/Osteoblast balance* | *Normalized metrics* |

---

## 📊 Model Performance

| Metric                                      | Value        |
|---------------------------------------------|--------------|
| **Overall Modulus (Graded Interface)**      | 29.2 MPa     |
| **Interface Toughness**                     | 9,835 J/m²   |
| **Stress Concentration Reduction**          | 0.0%*        |
| **Fatigue Life (3% strain)**                | 22,768 cycles|
| **Safety Factor (vs 100k target)**          | 0.23x        |
| **Differentiation Coverage (Day 28)**       | 0 → 1 gradient |

> *Note: Current abrupt vs graded comparison shows 0% reduction — indicating opportunity for gradient optimization.

---

## 📐 Gradient Profiles

| Profile Type    | Mathematical Form                          | Application              |
|----------------|--------------------------------------------|--------------------------|
| **Linear**     | `E = E_soft + (E_hard - E_soft) × (x/L)`   | Baseline comparison      |
| **Sigmoidal**  | Smoothstep interpolation (3t² - 2t³)       | **Biomimetic (default)** |
| **Exponential**| `E_soft × exp(β × t) / exp(β) × E_hard`    | Rapid transition         |

**Parameters:**
- Interface length: 10 mm
- Soft modulus: 10 MPa (tendon-like)
- Hard modulus: 1000 MPa (bone-like)

---

## ⚙️ How It Works

The simulation is structured into five integrated computational modules:

### 1️⃣ Stiffness Gradient Design
Defines continuous modulus variation from soft tendon to hard bone using analytical gradient functions. Three profiles are available: linear, sigmoidal (biomimetic), and exponential.

### 2️⃣ Mechanical Simulation
- **Stress Distribution**: Calculates local stress under uniform tensile strain.
- **Stress Concentration Factor (SCF)**: Compares graded vs abrupt interfaces.
- **Shear-Lag Analysis**: Models stress transfer efficiency and interface toughness.

### 3️⃣ Biological Simulation
- **Cell Seeding**: Tenocytes (soft region) and osteoblasts (hard region).
- **Differentiation**: Time-dependent conversion (21-day half-life).
- **Outputs**: Cell density profiles, proliferation kinetics, differentiation heatmaps.

### 4️⃣ Fatigue Life Prediction
- **S-N Curve**: Basquin equation (`σ_f = 100 MPa`, `b = -0.12`).
- **Stiffness Degradation**: Linear damage accumulation.
- **Outputs**: Fatigue life distribution, critical zone identification, safety factor.

### 5️⃣ Summary & Visualization
Generates a comprehensive dashboard with performance radar chart and key metrics.

---

## 🖥️ Technology Stack

| Component          | Technology                          |
|--------------------|-------------------------------------|
| **Language**       | Python 3.12                         |
| **Numerical Computing** | NumPy 2.0.2                      |
| **Scientific Computing** | SciPy 1.16.3 (integration, optimization) |
| **Visualization**  | Matplotlib 3.10.0                   |
| **Environment**    | Google Colab / Local Python         |

---

