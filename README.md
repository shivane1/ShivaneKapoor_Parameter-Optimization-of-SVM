# ShivaneKapoor_102203191_Parameter-Optimization-of-SVM

🔍 SVM Hyperparameter Tuning on Letter Recognition Data
This project explores Support Vector Machine (SVM) optimization using RandomizedSearchCV on the classic Letter Recognition dataset. The goal is to identify the best-performing model configurations using various randomized train-test splits, evaluate generalization performance, and track optimization behavior visually.

📂 Project Overview
Load and preprocess the Letter Recognition dataset from UCI (via OpenML)

Generate 10 unique train-test splits with stratified sampling (70% train, 30% test)

Perform SVM tuning using RandomizedSearchCV (10 iterations, 3-fold CV)

Track simulated convergence accuracy trends across 100 steps

Generate tabular performance summaries and a convergence graph

Save detailed results including analytics and model metrics

📊 Dataset Summary

Attribute	Description
Dataset Name	Letter Recognition
Samples	20,000
Features	16 (real-valued)
Target Classes	26 (Alphabets A–Z)
Source	UCI Repository / OpenML
🛠️ Technologies & Libraries
Python for implementation

scikit-learn for modeling and optimization

pandas, numpy for data manipulation

matplotlib for visualizations

RandomizedSearchCV for efficient parameter space exploration

🧠 Model Configuration & Tuning
We trained an SVC model for each of the 10 dataset splits with the following configuration:


Parameter	Values Tested
Kernel	'rbf', 'linear'
C	0.1, 1, 10
Gamma	'scale', 'auto'
CV Folds	3
Iterations	10 random combinations
✨ Convergence is simulated by interpolating sorted cross-validation scores over 100 steps.

📈 Sample Convergence Visualization
Below is the simulated convergence plot for the best-performing sample, showing how accuracy improved during parameter exploration:



🧾 Summary of SVM Optimization Results
Each row represents the best performance for one of the 10 samples:



Includes:

Accuracy on test set

Optimal hyperparameters: kernel, C, gamma

📌 Additional Analysis
A brief analytics summary is generated and stored:

Dataset size and class count

Best-performing sample ID

Corresponding accuracy and SVM configuration



🚀 Future Enhancements (New Section)
Add support for Polynomial and Sigmoid kernels

Include GridSearchCV vs RandomizedSearchCV comparison

Visualize misclassifications using confusion matrices

Track training time for each parameter configuration

Perform feature importance analysis (e.g., via PCA)

✅ Conclusion
This experiment highlights how even a simple SVM model, when tuned correctly, can yield strong performance on complex multiclass problems like character recognition. The pipeline is efficient, extensible, and serves as a template for future SVM-based tuning workflows.

