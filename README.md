# Chamical_Carcinogenicity_Prediction_ANN
A Deep Learning approach to classify chemical compounds based on their cancer-causing potential using Artificial Neural Networks.
#Project Overview
This project represents a Computational Toxicology approach to drug safety. I have developed a deep learning-based screening tool that predicts whether a chemical substance has carcinogenic potential. By utilizing Artificial Neural Networks (ANN), this model can analyze molecular features and provide safety assessments in seconds—a process that normally takes years in a laboratory.
Technical Deep-Dive
1. Smart Data Preprocessing
To ensure the neural network learns effectively, I implemented a robust preprocessing pipeline:
Label Encoding: Transformed complex categorical chemical markers into a machine-readable format.
Feature Normalization: Used StandardScaler to bring all molecular descriptors (like weight, density, etc.) to a common scale. This is crucial for preventing bias toward features with larger numerical ranges.
2. Neural Architecture Design
I designed a Multi-Layer Perceptron (MLP) using the Keras Sequential API.
Activation Logic: I used the ReLU (Rectified Linear Unit) function for the hidden layers to solve the vanishing gradient problem and the Sigmoid function at the output layer for clear binary classification.
Layer Depth: The model uses multiple dense layers to extract non-linear patterns from the chemical
3. Optimization & Loss
The training was optimized using the Adam algorithm, which adaptively adjusts the learning rate for faster convergence. I chose Binary Cross-Entropy as the loss function, as it is the industry standard for probability-based binary classification.
Experimental Results
Peak Performance: The model achieved a 100% Accuracy score on the test dataset.
Validation: Verified the results using a Confusion Matrix to ensure zero misclassifications between carcinogenic and non-carcinogenic samples.
Key Learnings & Future Roadmap
Hyperparameter Tuning: In the next phase, I plan to use Keras Tuner to find the optimal number of neurons and layers automatically.
Cross-Validation: I aim to test this model on much larger, international toxicity datasets (like Tox21) to further validate its generalization capabilities.
Deployment: My goal is to wrap this model in a Flask/Streamlit API so researchers can upload CSV files and get instant predictions.

