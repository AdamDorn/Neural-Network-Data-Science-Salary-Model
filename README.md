Data Science Salary Fairness Classification Project
Objective
The aim of this project is to classify whether a given salary is fair or underpaid based on features such as job title, location, experience, and other relevant factors. Using deep learning, we explore different neural network architectures to identify an optimal model that achieves strong classification performance.

Dataset Description
The dataset includes labeled examples indicating salary fairness (fair or underpaid).

Input features were preprocessed and transformed into a dense numeric format suitable for neural network input.

Model Architectures
We experimented with three variations of feedforward neural networks:

Model V1 (Baseline Model)

Dense Layer: 64 units, ReLU activation

Dense Layer: 32 units, ReLU activation

Output Layer: 1 unit, Sigmoid activation

Optimizer: Adam (learning rate = 0.001)

Epochs: 25

Batch size: 64

Model V2 (Deeper Network without Regularization)

Dense Layer: 128 units, ReLU

Dense Layer: 64 units, ReLU

Dense Layer: 32 units, ReLU

Output Layer: 1 unit, Sigmoid

Same optimizer and training settings as Model V1

Model V3 (Regularized Model)

Dense Layer: 64 units, ReLU + L2 regularization (λ = 0.01)

Dropout: 0.5

Dense Layer: 32 units, ReLU + L2 regularization (λ = 0.01)

Dropout: 0.5

Output Layer: 1 unit, Sigmoid

Evaluation Metrics
All models were evaluated using:

Test Accuracy

Training vs. Validation Loss Curves

Confusion Matrix

ROC Curve and AUC Score

Results Summary
Model	Test Accuracy	ROC AUC	Notes
V1	88.2%	0.94	Best-performing architecture
V2	51.0%	~0.5	No meaningful learning, likely overfitting or instability
V3	51.0%	~0.5	Training stabilized by regularization, but no performance gain

Additional Observations:

Model V1: Healthy convergence with minimal overfitting; good balance between precision and recall.

Model V2: Accuracy hovered near random chance, indicating poor model performance.

Model V3: Regularization helped stabilize training but did not improve performance.

Conclusion
Model V1 outperformed the deeper and regularized variations by demonstrating strong classification performance, good generalization, and reliable training convergence. Models V2 and V3 failed to improve and performed close to random guessing.

Dataset Source
“The Global AI, ML, Data Science Salary (2020–2025)” by Samith Sachidanandan
Available on Kaggle: https://www.kaggle.com/datasets/samithsachidanandan/the-global-ai-ml-data-science-salary-for-2025
Licensed under CC0 Public Domain.
