## Latent Space Optimization for the 2D Ising Model

This project that applies Latent Space Optimization to approximate the ground state, minimum energy configuration of a 2D Ising Model.
The project was developed by the Optimization Techniques course in the Master in Computational Engineering and Smart Systems at the University of the Basque Country (EHU/UPV).

---

## How to Run

1. Clone or download this repository
2. Ensure you have Python 3.9+ installed and required dependencies
3. Open the notebook:

```bash
jupyter notebook ising_model_notebook.ipynb
```
---

## Project Overview

The Ising model is a classic problem in statistical physics and combinatorial optimization. In this project:

* A 20×20 2D Ising grid is used, with spins taking values in ({-1, +1})
* Spins interact with their nearest neighbors through predefined coupling constants
* The objective is to minimize the Ising energy function
* Instead of direct optimization in configuration space, the problem is tackled using Latent Space Optimization, combining:
  
  * Data-driven representation learning
  * Surrogate modeling
  * Optimization in a reduced latent space

---

## Methodology

The notebook is structured into the following main steps:

1. **Define the Input and Objective Function**
   Representation of the Ising model and its energy function.

2. **Generate a Training Dataset**
   Creation of spin configurations (with a controllable bias toward ordered states).

3. **Learn the Latent Representation**
   Dimensionality reduction using an encoder–decoder architecture.

4. **Construct a Latent Objective Model (Surrogate)**
   A regression model that approximates energy values in latent space.

5. **Perform Latent Space Optimization**
   Optimization is carried out in the latent space instead of the original configuration space.

6. **Decoding and Evaluation**
   Optimized latent vectors are decoded back to spin configurations and evaluated.

---

## Results

Both optimization methods tested (Gradient Descent and CMA-ES) were run with multiple restarts and consistently found the ground state of the 2D Ising model. In all cases, the minimum energy configuration (E = -800) was successfully recovered, showing that the approach is reliable and not sensitive to initialization.

Check the final report to take a closer look on the achived results :)
