Iris Flower Species Classification Project
This project demonstrates a fundamental machine learning workflow using the classic Iris dataset and a Logistic Regression classifier. It is structured using a scikit-learn pipeline for clean and reproducible data processing and modeling.

💾 Dataset
Source: sklearn.datasets.load_iris()

Problem Type: Multi-Class Classification (3 Species: Setosa, Versicolor, Virginica)

Features: Sepal Length, Sepal Width, Petal Length, Petal Width.

⚙️ Dependencies
This script requires the following libraries:

pip install pandas scikit-learn seaborn matplotlib

🚀 How to Run
Save the Python code above as iris_classifier.py.

Execute from your terminal:

python iris_classifier.py

📋 Machine Learning Workflow
The script follows four main modular steps:

load_data(): Fetches and converts the raw data into a pandas DataFrame.

pre_process(): Splits the data (80% Train, 20% Test) using train_test_split with stratification to ensure balanced class representation.

build_pipeline(): Creates a simple Pipeline object containing the LogisticRegression model.

evaluate(): Trains the model and tests its performance on the hold-out test set.

✅ Model Evaluation Results
Due to the simplicity and high separability of the Iris dataset, the model achieves perfect classification on the test set:

Metric

Score

Note

Accuracy

1.0000

Proportion of correct predictions.

Precision

1.0000

Weighted precision across all classes.

Recall

1.0000

Weighted recall across all classes.

F1 Score

1.0000

Harmonic mean of Precision and Recall.

The script also generates a visual Confusion Matrix to confirm the flawless performance.