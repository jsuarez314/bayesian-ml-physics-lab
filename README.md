# bayesian-ml-physics-lab
Companion repository for the paper "Exploring Bayesian Inference and Physics-Informed Neural Networks in the Analysis of U-Tube Oscillations: A Pedagogical
Perspective". Includes code and examples using Bayesian inference and Physics-Informed Neural Networks (PINNs) to enhance parameter estimation in physics lab experiments.

---

## Run Notebooks in Google Colab

You can run the example notebooks directly in Google Colab by clicking the badges below.

### 1. U-Tube Fluid Dynamics Simulation
This notebook simulates the fluid dynamics of a U-tube.  
You can adjust parameters such as fluid density, damping coefficient, and initial heights.  
The simulation displays the U-tube, displacement, velocity, and phase space plots.  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1nb3eGUpHN7Cb0frBrsLhDLiui9a3pRlz?usp=sharing)

---

### 2. Bayesian Estimation of Position and Velocity
This notebook demonstrates how to estimate the **position** and **velocity** of an object using Bayesian inference with the `emcee` library.  
It walks through data generation, likelihood modeling, and parameter estimation.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ZDlHRoDN1_yvvaPJIKafEYG77uilO1Kp?usp=sharing)

### 3. PINN Estimation of Position and Velocity
This notebook applies a **Physics-Informed Neural Network (PINN)** to estimate the **position** and **velocity** of the oscillating fluid in the U-tube system.  
The model learns directly from data while enforcing the governing physical equation during training.  
It includes the construction of data and physics loss terms, joint optimization of the neural network and physical parameters (\(\mu\), \(\omega_0\)), and visualization of the model fit and parameter convergence.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/13zoAuB60XjPxfaYHmCIelch7qcP4ctdd?usp=sharing)
