# Autism Spectrum Disorder (ASD) Classification Using Support Vector Machine (SVM)

Overview :
This project aims to predict the presence of Autism Spectrum Disorder (ASD) in children based on various features, including social responsiveness, age, and other behavioral and medical conditions. A machine learning model using a Support Vector Machine (SVM) classifier is trained on a dataset, and predictions are made based on individual input data.

Key Features:

The dataset used for training contains multiple features:
Social Responsiveness Scale: Measures the level of social interaction.
Age in Years: The age of the individual.
Speech Delay/Language Disorder: Whether the individual has speech delay or language disorders.
Learning Disorder: Indicates the presence of a learning disorder.
Genetic Disorders: Presence of any genetic disorders.
Depression: Whether the individual has depression.
Global Developmental Delay/Intellectual Disability: Whether the individual has developmental delays or intellectual disabilities.
Social/Behavioral Issues: Social or behavioral challenges experienced by the individual.
Childhood Autism Rating Scale: A scale used to assess the severity of autism.
Anxiety Disorder: Whether the individual has anxiety.
Sex: Gender of the individual.
Jaundice: Whether the individual experienced jaundice.
Family Member with ASD: Whether there is a family history of autism.
Outcome: Target variable (1 for ASD, 0 for non-ASD).

Data Preprocessing:

The dataset is loaded from a CSV file containing 1961 rows and 14 columns, where each row represents a unique individual. The data is then analyzed to gain insights into its structure and distribution. The Outcome column is the target variable that indicates whether the individual has ASD (1) or not (0).
Statistical Analysis
The dataset is analyzed to obtain statistical measures such as mean, standard deviation, minimum, and maximum values for each feature.
The Outcome variable shows that there are 1056 individuals with ASD and 905 individuals without ASD.

Data Standardization:
The features are standardized using StandardScaler to ensure that all attributes have the same scale. This step is crucial for models like SVM to perform well since they are sensitive to the scale of the data.

Model Training:
Train-Test Split
The dataset is split into training and testing sets using an 80-20 split. The stratify parameter ensures that both classes (ASD and non-ASD) are represented proportionally in both training and testing datasets.

Model Selection:
A Support Vector Machine (SVM) classifier with a linear kernel is chosen for the task. SVM is effective for binary classification tasks and works well when the data is linearly separable.

Model Training:
The classifier is trained using the training data (X_train, Y_train). The trained model is then evaluated using accuracy metrics on both training and testing datasets.

Model Evaluation:
Training Accuracy
The model achieves an accuracy score of approximately 69.2% on the training data. This indicates that the model performs reasonably well in learning the patterns from the training set.
Testing Accuracy
The model achieves an accuracy score of around 73.0% on the testing data, which shows that the model generalizes well to unseen data.

Predictive System:
Making Predictions
The model is used to predict whether an individual has ASD or not based on input data. New input data is standardized using the same scaler and then passed through the trained model to obtain the prediction.

Example Input:
An example input is provided with features such as age, social responsiveness, speech delay, and others. The model processes the input, and based on the prediction, it indicates whether the individual is likely to have ASD or not.

Output:
The output from the prediction is a binary value (0 or 1):
0: The person is not with ASD.
1: The person is with ASD.
