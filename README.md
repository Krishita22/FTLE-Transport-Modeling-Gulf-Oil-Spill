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


2) Install dependencies
pip install -U pip
pip install numpy scipy matplotlib jupyter

If your notebooks use additional packages (e.g., pandas, seaborn), add them too:

pip install pandas seaborn scikit-learn
▶️ How to Run
jupyter notebook

Open any .ipynb file and run cells top-to-bottom.

Suggested order:

Start with Red.ipynb, Blue.ipynb, or GreenYellow.ipynb

Then try pulsing versions (e.g., RedPulsing.ipynb)

Finally compute FTLE fields in FTLE.ipynb

🧪 Notes / Tips

Use small notebooks (*Small.ipynb) when testing parameters quickly.

Pulsing notebooks are helpful to study time-dependent perturbations and how they change mixing/transport barriers.

If a notebook is slow, reduce:

grid resolution

integration time window

number of particles

🗺️ Results (What You’ll See)

Outputs generally include:

Particle trajectory plots

Phase-space / spatial deformation behavior

FTLE heatmaps / contours

Comparison of pulsed vs non-pulsed flow structure

These visualizations highlight coherent transport barriers and mixing regions.

🧩 Future Work

Add explicit SDE noise models + uncertainty quantification

Extract LCS ridges automatically from FTLE fields

Parameter sweeps + reproducible experiment configs

Speedups (vectorized integrators / GPU)

👩‍💻 Author

Krishita Vaghani
B.S. Computer Science, Minor in Mathematics
Applied Math / Dynamical Systems Research

📜 License

For academic and research use.
