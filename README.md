# Black-Box Optimisation Capstone Project - Machine Learning & Artificial Intelligence 


## NON-TECHNICAL EXPLANATION OF YOUR PROJECT

The Black-Box Optimization Capstone project applied machine learning (ML) to maximize several functions. This project was developed over 13 weeks, during which various methods were implemented, with the ability to control trial and error being key.
This aproach can be usefull in real-world problems (e.g., pollution, medicine, business, etc.) because by observing the behavior of a system, entity, or user and optimizing a key outcome based on those observations. 


## DATA

The dataset in this project consist in eight functions where each feature will have increasing dimensionality (from 2D to 8D). 

Each data point consists: 

Inputs are initially represented by known data points (x, y); this initial set is crucial for the initial training of the model and establishes a baseline. Each week, the number of data points increases. This simulates a real-life scenario where data is constantly collected over time. This new data is essential for the model to learn and adapt to a larger feature space and improve its optimization.

Output is the result of the optimization process, where the output will be a single value for each feature


## MODEL

The main model used in the final project was Bayesian Optimization (BO), whose effectiveness lies in optimizing complex or black-box functions that require considerable computation time. BO works by building a probabilistic model (the surrogate model, in this case, a Gaussian process) of the objective function and then using an acquisition function to determine the next most promising point for evaluation.


## HYPERPARAMETER OPTIMSATION

During hyperparameter tuning, the following key hyperparameters were explored
Gaussian Process Kernel Parameters (C, RBF length_scale and bounds): a combination of a ConstantKernel (C) and a RadialBasisFunction (RBF) kernel is a common and flexible choice for GPR. The ConstantKernel accounts for the overall magnitude of the function, while the RBF kernel captures the smoothness and correlation between data points. 
Acquisition Function Parameters (kappa for UCB, xi for PI and EI): these parameters control the exploration-exploitation trade-off in the acquisition functions.
These hyperparameters were prioritized to ensure the Gaussian Process was robust, numerically stable, and capable of effectively modeling the objective function, while the acquisition function parameters were chosen to balance exploration and exploitation during the Bayesian Optimization process.
