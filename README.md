
# Diabetes Prediction using Machine Learning

![Test Image 1](https://d18yrmqbzi0q7a.cloudfront.net/wp-content/uploads/diabetes-symptoms-and-treatment.jpg)

Diabetes refers to a group of metabolic disorders characterized by elevated blood sugar levels over an extended period. Common symptoms of high blood sugar include frequent urination, increased thirst, and heightened hunger. Without proper treatment, diabetes can lead to a range of complications. It could even lead to death. Over the long term, diabetes can cause serious health issues such as cardiovascular disease, stroke, chronic kidney disease, foot ulcers, and damage to the eyes.

# Objective
I will try to build a machine learning model that will predict whether a patient has diabetes or not a accurately as possible for a first-timer.

# Details about the dataset
The datasets consists of a handful medical independent variables and one dependent variable. The Outcome which is a binary variable determines whether or not the patient has diabetes. Predictor variables includes the number of pregnancies the patient has had, their BMI, insulin level, age, and several others. The dataset used in this study originates from the National Institute of Diabetes and Digestive and Kidney Diseases. The goal is to predict whether a patient has diabetes based on specific diagnostic measurements provided in the dataset. The dataset was carefully curated, including only females aged 21 years or older to make tests fair, all of whom are of Pima Indian heritage and obtained from Kaggle.

# Result 
I tested three different basic algorithms, including Logistic Regression, RandomForestClassifier and Support Vector Machine. In the end the classic Logistic Regression algorithm used for classification gave me the highest average Cross Validation Score of 77.5%. This is without any finetuning which is a skill I know about but have yet to utilise and fully grasp.
