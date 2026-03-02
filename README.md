# Physics-Informed Neural Network (PINN) for Thermal Modeling

## Objective
A proof-of-concept project demonstrating how Scientific Machine Learning can solve thermodynamic equations without traditional finite element meshes. 

This repository contains a PyTorch implementation of a Physics-Informed Neural Network designed to solve the 1D Heat Equation ($u_t = \alpha u_{xx}$). By embedding the governing laws of physics directly into the neural network's loss function, the model learns to predict thermal conduction accurately.

## Technical Stack
* **Language:** Python
* **Framework:** PyTorch
* **Libraries:** NumPy, Matplotlib

## Methodology
Instead of relying purely on massive datasets, this network is trained using:
1. **Boundary/Initial Conditions:** Known temperature states (e.g., cooling boundaries).
2. **Physics Loss:** A residual calculation using PyTorch's Automatic Differentiation (`torch.autograd`) to ensure the network's predictions strictly obey the heat equation at randomized collocation points.

## Future Scope
This 1D proof-of-concept serves as the foundational architecture for my ongoing research into predicting 3D internal thermal fields and degradation in cylindrical lithium-ion battery cells.
