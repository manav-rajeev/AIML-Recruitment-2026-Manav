# Coding Ninjas 10X Club – AI/ML Recruitment 2026

## Candidate Details

- **Name:** Manav Rajeev
- **Year:** Second Year
- **Program:** B.Tech CSE – Cybersecurity
- **Task:** Task 2 – Neural Network for MNIST Digit Classification

---

## Problem Statement

The objective of this task is to build a simple neural network using TensorFlow/Keras to classify handwritten digits from the MNIST dataset.

The task involves loading and preprocessing the dataset, building a baseline neural network, training and evaluating the model, visualizing its performance, and conducting an experiment by changing a model/training parameter.

---

## Approach

The project was implemented using the following steps:

1. Loaded the MNIST handwritten digit dataset.
2. Inspected the dataset dimensions and sample images.
3. Normalized pixel values from the range 0–255 to 0–1.
4. Flattened each 28 × 28 image into a vector of 784 features.
5. Built a simple fully connected neural network as the baseline model.
6. Trained the model using the Adam optimizer.
7. Evaluated the baseline model on the test dataset.
8. Visualized training and validation accuracy and loss.
9. Generated a confusion matrix to analyze classification errors.
10. Conducted an experiment by increasing the hidden-layer size from 128 to 256 neurons.
11. Compared the baseline and experimental models using test accuracy and test loss.
12. Documented the findings, limitations, and possible improvements.

Technologies Used
Python
TensorFlow
Keras
NumPy
Matplotlib
Scikit-learn
Google Colab
MNIST dataset

Training Configuration
Parameter	Value
Optimizer	Adam
Loss Function	Sparse Categorical Cross-Entropy
Metric	Accuracy
Epochs	10
Batch Size	32
Validation Split	0.1
Random Seed	42
Results
Baseline vs Experimental Model
Metric	Baseline – 128 Neurons	Experiment – 256 Neurons
Test Accuracy	97.28%	97.54%
Test Loss	0.1062	0.1016

The experimental model improved test accuracy by 0.26 percentage points and reduced test loss by 0.0046.

Interpretation

Increasing the hidden-layer size from 128 to 256 neurons gave the model additional capacity to learn patterns in the MNIST images. In this experiment, this resulted in a small improvement in performance on the unseen test data.

However, increasing the number of neurons also increases the number of model parameters and computational requirements. A larger model does not automatically guarantee better generalization.

Confusion Matrix

The confusion matrix was used to examine which digits were classified correctly and which digits were confused with one another.

Most predictions were concentrated along the diagonal of the confusion matrix, indicating that the majority of test images were classified correctly.

Some misclassifications occurred between handwritten digits with similar visual patterns. One of the larger observed confusions was between actual digit 2 and predicted digit 3.

Key Learnings
Data preprocessing is important: Normalizing pixel values and flattening the images prepared the MNIST data for use with a fully connected neural network.
Model capacity affects performance: Increasing the hidden layer from 128 to 256 neurons produced a small improvement in test accuracy in this experiment.
Confusion matrices provide more information than accuracy alone: They show which individual classes are being confused by the model.
Experiments should change controlled variables: Keeping the other training settings constant made it possible to observe the effect of changing the hidden-layer size.
Challenges and Solutions
Challenge: Understanding the effect of model size

A larger neural network does not necessarily perform better. To investigate this, the hidden-layer size was changed from 128 to 256 neurons while keeping the other training settings unchanged.

The two models were then evaluated using the same MNIST test dataset and compared using test accuracy and test loss.

Limitations
The model is a simple fully connected neural network and does not explicitly exploit the spatial structure of images.
Only one model experiment was performed.
The experiment was conducted only on the MNIST dataset.
Different hyperparameters or architectures could produce different results.
Possible Future Improvements
Experiment with different learning rates, batch sizes, and numbers of epochs.
Investigate regularization techniques such as dropout.
Try a Convolutional Neural Network (CNN) for image classification.
Perform additional hyperparameter experiments.
Evaluate the approach on more challenging image datasets.
Conclusion

A simple fully connected neural network was developed to classify handwritten MNIST digits.

The baseline model achieved 97.28% test accuracy with a test loss of 0.1062. Increasing the hidden-layer size from 128 to 256 neurons resulted in 97.54% test accuracy and a test loss of 0.1016 in the experimental run.

The experiment demonstrates how changing a model parameter can affect its performance and highlights the importance of evaluating machine-learning models using both quantitative metrics and tools such as confusion matrices.
Dense Layer: 128 neurons + ReLU
        ↓
Dense Layer: 10 neurons + Softmax
