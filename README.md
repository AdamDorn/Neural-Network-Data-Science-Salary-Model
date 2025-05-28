**Data Science Salary Fairness Classification Project **
---

* Objective *
The aim of this project is to classify whether a given salary is fair or underpaid based on features such as job title, location, experience, and other relevant factors. Using deep learning, we explore different neural network architectures to identify an optimal model that achieves strong classification performance.

---

* Dataset Description *
The dataset includes labeled examples indicating salary fairness (fair or underpaid). The input features were preprocessed and transformed into a dense numeric format suitable for neural network input.

---

*Model Architectures*
We experimented with three variations of feedforward neural networks:

Model V1 (Baseline Model)
Dense Layer: 64 units, ReLU activation

Dense Layer: 32 units, ReLU activation

Output Layer: 1 unit, Sigmoid activation

Optimizer: Adam (lr=0.001)

Epochs: 25

Batch size: 64

Model V2 (Deeper Network without Regularization)
Dense Layer: 128 units, ReLU

Dense Layer: 64 units, ReLU

Dense Layer: 32 units, ReLU

Output Layer: 1 unit, Sigmoid

Same optimizer and training settings as Model V1

Model V3 (Regularized Model)
Dense Layer: 64 units, ReLU + L2 regularization (λ=0.01)

Dropout: 0.5

Dense Layer: 32 units, ReLU + L2 regularization (λ=0.01)

Dropout: 0.5

Output Layer: 1 unit, Sigmoid

---

* Evaluation Metrics *
All models were evaluated using:

Test Accuracy

Training vs. Validation Loss Curves

Confusion Matrix

ROC Curve and AUC Score

---

* Results Summary *
Model V1 (Best Performance)
Test Accuracy: 88.2%

ROC AUC: 0.94

Confusion Matrix: Good balance between precision and recall

Observations: Healthy convergence, minimal overfitting

Model V2 (Deeper Network)
Test Accuracy: 51.0%

Observations: Accuracy remained near random chance. Likely overfitting or model instability

Model V3 (Regularized)
Test Accuracy: 51.0%

Observations: Regularization helped training stabilize, but no performance gain observed

Accuracy Comparison
Model	Test Accuracy	ROC AUC	Notes
Model V1	88.2%	0.94	Best-performing architecture
Model V2	51.0%	~0.5	No meaningful learning
Model V3	51.0%	~0.5	Training stable, but weak

---

* Conclusion *
Model V1 outperformed the deeper and regularized variations. It demonstrated strong classification performance, good generalization, and reliable convergence during training. Models V2 and V3 failed to show improvements and hovered around random-guess accuracy.

---
