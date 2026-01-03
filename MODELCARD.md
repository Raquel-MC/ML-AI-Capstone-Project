# Model card for your BBO optimisation approach

### Overview
- Approach: The model approach is the Bayesian Optimization, using the Gaussian process model and acquisition function that goes between UCB (Upper Confident Bound) or EI (Expected Improvement) depending on the requirements.The current version is round 10
- Type: Black-Box-Optimisation
- Version: v1.0

### Intended use
The Black-Box Optimization (BBO) approach is primarily intended for scenarios where the internal mechanics of a system are unknown, unexploitable, or too complex to model mathematically.
- BBO is most effective for costly problems, where each evaluation requires significant time, money, or computational resources.
- BBO should be avoided or replaced in areas such as medical diagnosis or legal sentencing, as its "black box" nature can be a drawback if interpretability is a legal or ethical requirement.

### Details
The strategy was primarily exploration, as the priority was to reduce uncertainty by combining the Gaussian process model with the UCB (Upper Confidence Limit) acquisition function. 
Subsequently, once certain functions showed improved results, I moved to exploitation, maintaining the same Gaussian process model and changing the acquisition function to EI (Expected Improvement).

### Performance
Regarding the performance of the roles, I think it's fair to say that not all of them have responded in the same way. Therefore, based on their results so far, I could group them into two categories: 
- Stabilized / Improving: The surrogate model has successfully captured the general "slope" toward the optimum and each round provides more data that confirms the direction.
- Unstable / Uncertain: The algorithm might find one good spot, but then a new query suggests an even better spot far away, causing the search to jump around.

### Assumptions and limitations
- It assumes the initial exploration phase was broad enough to capture the true region of interest. If the initial sample points did not reach the main peak, the subsequent exploitation phase will only refine a false local optimum.
- The strategy assumes that the function's behavior does not change over time (stationarity). This means that a point that was optimal in round 2 might no longer be optimal in round 7.
- Noise levels are often assumed to be consistent throughout the search space.

### Ethical considerations
I do not see any major considerations, except that it would be wise to treat this approach with care if the idea is to use it in the real world, since the data was provided and the process is part of a competition.
