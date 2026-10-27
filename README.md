Phishing URL Detection Using Decision Tree
Project Overview

This project aims to detect whether a website URL is Phishing or Legitimate using a Decision Tree Classifier. The model is trained on a phishing URL dataset containing various website-related features and learns patterns that distinguish malicious URLs from genuine ones.
Objective

The main objective of this project is to:

    Classify URLs as Phishing or Legitimate.
    Apply Machine Learning techniques for cybersecurity.
    Evaluate model performance using classification metrics.
    Visualize the decision-making process of the Decision Tree.

Technologies Used

    Python
    Pandas
    NumPy
    Matplotlib
    Scikit-learn
    Jupyter Notebook

Dataset Information

The dataset contains 27,595 records and 56 features describing different characteristics of URLs and websites.
Sample Features

    URL Length
    Domain Length
    IsDomainIP
    URL Similarity Index
    Character Continuation Rate
    TLD
    Number of Redirects
    Has Copyright Information
    Has Social Network Links
    Word Count Features
    Embedded Brand Names

Target Variable
Label 	Meaning
0 	Legitimate Website
1 	Phishing Website
Data Preprocessing

The following preprocessing steps were performed:

    Loaded the dataset using Pandas.
    Checked dataset dimensions.
    Identified and handled missing values.
    Encoded target labels:
        Legitimate → 0
        Phishing → 1
    Replaced missing numeric values with column means.
    Split features and target variables.

Model Building

A Decision Tree Classifier was used with:

DecisionTreeClassifier(
    max_depth=5,
    class_weight='balanced',
    random_state=42
)

Train-Test Split

    Training Data: 80%
    Testing Data: 20%

train_test_split(
    X,
    y,
    test_size=0.20,
    random_state=42,
    stratify=y
)

Decision Tree Visualization

The trained Decision Tree was visualized using Scikit-learn's plot_tree() function to understand the decision-making process.

plot_tree(
    model,
    feature_names=X.columns,
    class_names=['Legitimate', 'Phishing'],
    filled=True
)

Model Evaluation

The model was evaluated using:

    Accuracy Score
    Precision Score
    Recall Score
    F1 Score
    Confusion Matrix
    Specificity

Confusion Matrix
Actual / Predicted 	Legitimate 	Phishing
Legitimate 	26970 	0
Phishing 	0 	20189
Results
Metric 	Score
Accuracy 	1.0000
Precision 	1.0000
Recall 	1.0000
F1 Score 	1.0000
Specificity 	1.0000
Interpretation

The Decision Tree model achieved perfect classification performance on the test dataset, correctly identifying all phishing and legitimate URLs without any misclassifications.
Project Workflow

    Data Collection
    Data Exploration
    Data Cleaning
    Feature Selection
    Train-Test Split
    Model Training
    Prediction
    Evaluation
    Decision Tree Visualization

Folder Structure

Phishing-URL-Detection/
│
├── dataset/
│   └── Phishing_Legitimate_Full.csv
│
├── notebooks/
│   └── Untitled14.ipynb
│
├── images/
│   ├── decision_tree.png
│   └── confusion_matrix.png
│
├── README.md
└── requirements.txt

How to Run
Install Dependencies

pip install pandas numpy matplotlib scikit-learn

Run Jupyter Notebook

jupyter notebook

Open:

Untitled14.ipynb

and run all cells.
Future Improvements

    Random Forest Classifier
    XGBoost Classifier
    Real-time URL Scanning
    Flask Web Application
    Browser Extension Integration
    Feature Engineering for improved robustness

Conclusion

This project demonstrates how Machine Learning can be used in cybersecurity to detect phishing websites. Using a Decision Tree Classifier, the model successfully learned URL patterns and achieved excellent performance in distinguishing phishing URLs from legitimate ones.
Author

Arockiya Jeniliya BCA Student
