# Stochastic Flow Analysis & FTLE Research

Research code for analyzing **stochastic dynamical systems** and **Lagrangian Coherent Structures (LCS)** using **Finite-Time Lyapunov Exponents (FTLE)**.  
These notebooks explore transport, mixing, and coherent structures in multi-blob / multi-gyre style flows under **time-dependent pulsing** and different configurations (Red/Blue/Green-Yellow variants).

---

## ✨ What’s Inside

This repo focuses on:

- **FTLE field computation** to detect coherent structures (LCS ridges)
- **Particle trajectory integration** under time-dependent flows
- **Flow-map deformation analysis** (Cauchy–Green tensor)
- Comparing base flows vs **pulsing / perturbed** variants
- Small-domain variants for faster iteration and controlled experiments

---

## 📁 Notebooks Included

### Core FTLE Analysis
- `FTLE.ipynb` — FTLE computation + visualization

### Base Flow Configurations
- `Red.ipynb`
- `Blue.ipynb`
- `GreenYellow.ipynb`

### Pulsing / Time-Dependent Perturbations
- `RedPulsing.ipynb`
- `BluePulsing.ipynb`
- `GreenYellowPulsing.ipynb`
- `RedDiffPosPulsing.ipynb`

### Blob-Based Flow Experiments
- `RedBlob.ipynb`

### Small-Domain / Compact Versions
- `RedSmall.ipynb`
- `BlueSmall.ipynb`
- `GreenSmall.ipynb`
- `RPSmall.ipynb`
- `BPSmall.ipynb`
- `GPSmall.ipynb`

---

## 🧠 Method (High Level)

FTLE is computed from the flow map over a finite time window \(T\).

Particles are integrated forward (or backward), the **flow map gradient** is estimated, and the maximum stretching rate is extracted via the **Cauchy–Green deformation tensor**.

$$
\text{FTLE} = \frac{1}{|T|} \ln \sqrt{\lambda_{\max}}
$$

where $\lambda_{\max}$ is the largest eigenvalue of the Cauchy–Green deformation tensor.
---

## ✅ Setup

### 1) Create an environment (recommended)

```bash
python -m venv .venv
source .venv/bin/activate   # macOS/Linux
# .venv\Scripts\activate    # Windows
```

### 2) Install dependencies

```bash
pip install -U pip
pip install numpy scipy matplotlib jupyter
```

Optional:

```bash
pip install pandas seaborn scikit-learn
```

---

## ▶️ How to Run

```bash
jupyter notebook
```

Open any `.ipynb` file and run cells top-to-bottom.

### Suggested Order

1. `Red.ipynb`
2. `Blue.ipynb`
3. `GreenYellow.ipynb`
4. Pulsing variants (e.g., `RedPulsing.ipynb`)
5. `FTLE.ipynb`

---

## 🧪 Notes

- Use `*Small.ipynb` notebooks for faster parameter testing.
- Pulsing notebooks analyze time-dependent perturbations and transport barrier changes.
- If performance is slow, reduce:
  - Grid resolution
  - Integration time window
  - Number of particles

---

## 🗺️ Results

Outputs include:

- Particle trajectory plots
- Phase-space / spatial deformation behavior
- FTLE heatmaps / contour plots
- Comparison of pulsed vs non-pulsed flow structure

These visualizations highlight coherent transport barriers and mixing regions.

---

## 🧩 Future Work

- Explicit SDE noise models + uncertainty quantification
- Automatic LCS ridge extraction
- Parameter sweeps + reproducible experiment configurations
- Performance optimizations (vectorized integrators / GPU)

---

## 👩‍💻 Author

Krishita Vaghani  
B.S. Computer Science, Minor in Mathematics  
Applied Math / Dynamical Systems Research  

---

## 📜 License

For academic and research use.
