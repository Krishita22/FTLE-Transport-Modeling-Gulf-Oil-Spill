# FTLE-Transport-Modeling-Gulf-Oil-Spill

Stochastic Flow Analysis & FTLE Research

This repository contains research code for analyzing stochastic dynamical systems and Lagrangian coherent structures (LCS) using Finite-Time Lyapunov Exponents (FTLE). The simulations explore transport, mixing, and almost invariant sets in multi-gyre and blob-based flow environments under deterministic and stochastic forcing.

This work was developed as part of applied mathematics research in dynamical systems and fluid transport modeling.

Overview

The project investigates:

Finite-Time Lyapunov Exponents (FTLE)

Lagrangian Coherent Structures (LCS)

Transport barriers in time-dependent flows

Pulsing perturbations in multi-blob systems

Effects of stochastic forcing on invariant structures

The simulations visualize how particles evolve under different flow configurations (Red, Blue, Green, Pulsing variants, etc.) and how coherent structures emerge over finite time intervals.

Research Motivation

Understanding transport in time-dependent flows is critical for:

Ocean transport modeling

Atmospheric dynamics

Environmental risk analysis

Flow control strategies

Almost invariant set stabilization

FTLE fields help identify ridges that act as transport barriers, revealing coherent structures in complex systems.

Repository Structure
Core Analysis

FTLE.ipynb
Computes finite-time Lyapunov exponent fields for the flow configurations.

Flow Configurations
Base Flows

Red.ipynb

Blue.ipynb

GreenYellow.ipynb

Blue.ipynb

Small-Domain Variants

RedSmall.ipynb

BlueSmall.ipynb

GreenSmall.ipynb

RPSmall.ipynb

BPSmall.ipynb

GPSmall.ipynb

Pulsing / Time-Dependent Perturbations

RedPulsing.ipynb

BluePulsing.ipynb

GreenYellowPulsing.ipynb

RedDiffPosPulsing.ipynb

Blob-Based Flow

RedBlob.ipynb

Each notebook explores trajectory evolution, flow structure, and deformation behavior under different parameters.

Methods

The computational framework includes:

Numerical integration of particle trajectories

Flow map computation over finite time intervals

Jacobian estimation of the flow map

Largest singular value extraction

FTLE field computation:

FTLE
=
1
∣
𝑇
∣
ln
⁡
𝜆
max
⁡
FTLE=
∣T∣
1
	​

ln
λ
max
	​

	​


where 
𝜆
max
⁡
λ
max
	​

 is the maximum eigenvalue of the Cauchy–Green deformation tensor.

Requirements

Python 3.9+

Recommended libraries:

numpy
scipy
matplotlib
seaborn
scikit-learn

Install dependencies:

pip install -r requirements.txt
How to Run

Clone the repository:

git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

Launch Jupyter:

jupyter notebook

Open any notebook and execute cells sequentially.

Key Concepts Demonstrated

Stretching and folding mechanisms in nonlinear flows

Emergence of LCS ridges in FTLE fields

Sensitivity to initial conditions

Effects of time-dependent pulsing

Influence of domain size on transport structure

Sample Output

Outputs include:

Particle trajectory plots

Phase space evolution

FTLE contour maps

Comparative analysis between pulsed and non-pulsed flows

These visualizations highlight coherent transport barriers and mixing regions.

Future Extensions

Incorporating stochastic noise explicitly in SDE form

Uncertainty quantification for FTLE ridges

Control strategies for increasing invariance of coherent sets

GPU acceleration for large-scale FTLE grids

Author

Krishita Vaghani
B.S. Computer Science, Minor in Mathematics
Applied Mathematics & Dynamical Systems Research

License

This repository is intended for academic and research use.
