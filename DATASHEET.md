# Datasheet for your BBO capstone project data set.

### Motivation
This dataset was created to develop a Black Box Optimization (BBO) challenge. A data sheet serves as a standardized identity document for the dataset, detailing its origin, characteristics, and intended uses. Since BBO involves optimizing costly and unknown functions with a limited budget, clear documentation is vital for both trust and technical rigor.

### Composition
The dataset contains eight independent functions with dimensionality from 2D to 8D, with a range of [0,1]. They start with initial data points (X) and initial target values ​​(y), and their data increases in each round.

### Collection process
The documentation would detail the key outputs generated primarily by Bayesian optimization: 
Trained GP Model -> Acquisition Function Values -> Recommended Next Query Points -> Optimization History -> Visualizations -> Overall Best Observed Value -> Optimal Input Point -> Best Performing Acquisition Function -> Black-Box-Function

### Preprocessing and uses
No preprocessing is needed because the input values ​​are already between 0 and 1, already in the "optimal" format for most surrogate models (such as Gaussian processes) used in BBO.

### Distribution and maintenance
The author will maintain the dataset until the BBO challenge is complete. Afterward, it will be available in this Git repository for public use, but no maintenance will be performed.
