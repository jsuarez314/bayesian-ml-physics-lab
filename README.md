# bayesian-ml-physics-lab

Companion repository for the paper:  
**"Comparative Parameter Estimation in a Damped U-Tube Oscillator Using Bayesian Inference and Bayesian Physics-Informed Neural Networks"**

This repository provides the fully reproducible code, datasets, and interactive notebooks used to generate the results and figures presented in the paper. It includes two Bayesian inference routes applied to the same experimental dataset: analytic inference via MCMC, and a Bayesian Physics-Informed Neural Network (B-PINN). Bayesian model comparison over four candidate damping laws is also included. All materials are released under an open-source license (MIT) to facilitate reuse, adaptation, and extension by the research community.

---

## Repository Contents

The repository contains three Google Colaboratory notebooks that implement the core methods of the study, along with the experimental data used for parameter estimation.

| Notebook | Description |
|----------|-------------|
| [`01-U-Tube.ipynb`](https://drive.google.com/file/d/1j-SIv3ufXyBPTma2EZL8PEwiUUzpVnXr/view?usp=sharing) | Interactive simulation of the damped U-tube oscillator. Users can modify physical parameters (fluid density, damping coefficient, initial heights, cross-sectional area) and observe the effects on displacement, velocity, and the phase-space trajectory. |
| [`02-Bayesian-Estimation.ipynb`]() | Analytic Bayesian inference of the damped oscillator using the `emcee` MCMC sampler. The notebook loads the experimental data, defines the log-likelihood with an inferred noise scale, runs the affine-invariant ensemble sampler, and produces corner plots with parameter posteriors and credible intervals. It also implements the Bayesian model comparison over the four candidate damping laws (linear, quadratic, Duffing, Coulomb). |
| [`03-BPINN-Estimation.ipynb`]() | Bayesian Physics-Informed Neural Network implementation in PyTorch. The network learns the displacement while respecting the governing ODE, with priors on the network weights and on the physical parameters, and the physics residual treated as virtual observations. Hamiltonian Monte Carlo is used to sample the posterior. The notebook reproduces the noise/model-error separation and the Coulomb-kernel analysis discussed in the paper. |

All notebooks are designed to run directly in Google Colaboratory with **no local installation required**. The repository also includes the experimental dataset (U-tube displacement measurements) used in the paper, stored in the `data/` folder.

---

## Run the Notebooks

Click the badges below to open each notebook in Google Colab:

| Notebook | Colab Badge |
|----------|-------------|
| **01 – U-Tube Simulation** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1nb3eGUpHN7Cb0frBrsLhDLiui9a3pRlz) |
| **02 – Bayesian Estimation** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]() |
| **03 – B-PINN Estimation** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]() |

To run locally, clone this repository and install the required Python packages listed in `requirements.txt`.

---

## Data Availability

The experimental displacement data used in the paper are provided in the `data/` directory as a CSV file. The dataset corresponds to a damped oscillation recorded from a U-tube manometer (sampling frequency 20 Hz). Eight independent recordings of the same apparatus are included, with initial amplitudes in the range 21–55 mm; the recording analysed throughout the paper is labelled U1. Detailed information about the experimental setup can be found in the paper and in the references therein.

---

## License

This repository is distributed under the MIT License. See `LICENSE` for details.