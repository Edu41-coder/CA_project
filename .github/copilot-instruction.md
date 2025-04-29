Challenge goals
The Multi-Risk Agricultural Contract, managed by Pacifica, is designed for farmers to protect their farms. It provides coverage for professional activities, damage to farm buildings, stored equipment, and financial and legal protection. This ensures that in the event of a loss, the insured can maintain the continuity of their operations, both materially and financially.

Currently, fire risk accounts for a significant portion of the claims associated with the Multi-Risk Agricultural Contract, making it a critical challenge to model accurately.
The objective is to develop the best model to predict the pure fire premium, using:

A model for Frequency,
A model for Average Cost.
The final target variable, the charge, is calculated by multiplying the frequency, the average cost, and the number of years since the contract was taken out (the variable “ANNEE_ASSURANCE”).

Data description
A supplementary file is provided containing all available variables along with their descriptions. This file includes:

Target variables: FREQ, CM, and CHARGE
Geographical data: department, weather information, etc.
Contract-specific data, including:
The insured’s activity (e.g., farmer, polycultivator, etc.)
Guarantee subscription indicators
Number of buildings, employees, and claims declared at subscription
Surface data: areas of buildings (e.g., livestock, farm buildings), anonymized as surface1, surface2, etc., for confidentiality
Capital data: insured capital for specific options (e.g., theft, greenhouses), anonymized as capital1, capital2, etc.
Prevention data: information on preventive measures (e.g., presence of extinguishers, use of wood in structures), anonymized as prev1, prev2, etc., for confidentiality

Benchmark description
Challenge Objective

The goal of this challenge is to compare the performance of the models developed during this competition with that of a baseline model based on Generalized Linear Models (GLMs).

Benchmark Structure
The benchmark consists of two separate GLMs:

Claim Frequency:

Distribution: Poisson
Link Function: Log
Average Claim Cost:

Distribution: Tweedie
Link Function: Log
Evaluation
The evaluation of the models will rely on a single metric: RMSE (Root Mean Square Error), defined as:
​


where:

yᵢ represents the actual value,
ŷᵢ represents the predicted value,
n is the number of observations.
The idea is to assess how well the proposed approaches exceed the baseline models in terms of:

Prediction accuracy,
Interpretability and efficiency,
Business constraints associated with the task.