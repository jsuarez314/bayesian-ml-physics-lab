# bayesian-ml-physics-lab

Companion repository for the paper:  
**"Comparative Analysis of Bayesian Inference and Physics-Informed Neural Networks for Parameter Estimation in a Damped Oscillator: An Open-Science Approach"**  

This repository provides the **fully reproducible code, datasets, and interactive notebooks** used to generate the results and figures presented in the paper. All materials are released under an open‑source license (MIT) to facilitate reuse, adaptation, and extension by the research community.

---

## Repository Contents

The repository contains three Google Colaboratory notebooks that implement the core methods of the study, along with the experimental data used for parameter estimation.

| Notebook | Description |
|----------|-------------|
| [`01-U-Tube.ipynb`](https://colab.research.google.com/drive/1nb3eGUpHN7Cb0frBrsLhDLiui9a3pRlz) | Interactive simulation of the damped U‑tube oscillator. Users can modify physical parameters (amplitude, damping coefficient, natural frequency) and observe the effects on displacement, velocity, and phase space. |
| [`02-Bayesian-Estimation.ipynb`](https://colab.research.google.com/drive/1ZDlHRoDN1_yvvaPJIKafEYG77uilO1Kp) | Bayesian inference using the `emcee` MCMC sampler. The notebook loads the experimental data, defines the likelihood and priors, runs the chains, and produces corner plots with parameter posteriors and credible intervals. |
| [`03-PINN-Estimation.ipynb`](https://colab.research.google.com/drive/13zoAuB60XjPxfaYHmCIelch7qcP4ctdd) | Physics‑Informed Neural Network (PINN) implementation in PyTorch. The network learns the displacement while respecting the governing ODE. Training includes the physics loss, and the final estimates of $\gamma$ and $\omega_0$ are extracted. |

All notebooks are designed to run directly in Google Colaboratory with **no local installation required**. The repository also includes the experimental dataset (U‑tube displacement measurements) used in the paper, stored in the `data/` folder.

---

## Run the Notebooks

Click the badges below to open each notebook in Google Colab:

| Notebook | Colab Badge |
|----------|-------------|
| **01 – U-Tube Simulation** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1nb3eGUpHN7Cb0frBrsLhDLiui9a3pRlz?usp=sharing) |
| **02 – Bayesian Estimation** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ZDlHRoDN1_yvvaPJIKafEYG77uilO1Kp?usp=sharing) |
| **03 – PINN Estimation** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1LCZ345Gx9bCQFPe73BuPorTkZKxBsSOA/view?usp=sharing) |

To run locally, clone this repository and install the required Python packages listed in `requirements.txt`.

---

## Data Availability

The experimental displacement data used in the paper are provided in the `data/` directory as a CSV file. The dataset corresponds to a damped oscillation recorded from a U‑tube manometer (sampling frequency 20 Hz). Detailed information about the experimental setup can be found in the paper and in the references therein.
