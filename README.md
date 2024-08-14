
# Diabetes Prediction using Machine Learning

![Test Image 1](diabetes-symptoms-and-treatment.jpg)

Diabetes refers to a group of metabolic disorders characterized by elevated blood sugar levels over an extended period. Common symptoms of high blood sugar include frequent urination, increased thirst, and heightened hunger. Without proper treatment, diabetes can lead to a range of complications. It could even lead to death. Over the long term, diabetes can cause serious health issues such as cardiovascular disease, stroke, chronic kidney disease, foot ulcers, and damage to the eyes.

# Objective
I will try to build a machine learning model that will predict whether a patient has diabetes or not a accurately as possible for a first-timer. I will then use streamlit library to allow a user to insert values on a browser. I also took inspiration from https://github.com/ahmetcankaraoglan/Diabetes-Prediction-using-Machine-Learning/blob/main/Diabetes%20Prediction%20using%20Machine%20Learning/Diabetes%20Prediction%20using%20Machine%20Learning.ipynb

# Details about the dataset
The datasets consists of a handful medical independent variables and one dependent variable. The Outcome which is a binary variable determines whether or not the patient has diabetes. Predictor variables includes the number of pregnancies the patient has had, their BMI, insulin level, age, and several others. The dataset used in this study originates from the National Institute of Diabetes and Digestive and Kidney Diseases. The goal is to predict whether a patient has diabetes based on specific diagnostic measurements provided in the dataset. The dataset was carefully curated, including only females aged 21 years or older to make tests fair, all of whom are of Pima Indian heritage and obtained from Kaggle.

# Result 
I tested three different basic algorithms, including Logistic Regression, RandomForestClassifier and Support Vector Machine. In the end the classic Logistic Regression algorithm used for classification gave me the highest average Cross Validation Score of 77.5%. This is without any finetuning which is a skill I know about but have yet to utilise and fully grasp.

# Report on what I have learnt
Going through this project from start to finish, and doing something practically is truly a lot more rewarding and a lot more fruitful than going through the theory of it. I am not saying that the theory behind Machine Learning is useless; in fact there were a lot of things I learnt from going through the book of "Machine Learning for Beginners" especially when it comes to how the algorithms work. However, we live in a day and age where libraries in the Python Language such as Sci-Kit learn make it *almost* avoidable. I say almost because theory is still the backbone of the field especially with the Maths and Statistics behind it.

Anyway, enough on the theory vs practice. As you can see, I made sure that my first project in ML would be related to the medical field since I truly do love this sector from when I was in high-school. 

## The Dataset
The dataset was taken from Kaggle and using the Pandas library, I was able to determine several features about it. Such as: the number of rows and columns, rows meaning the number of data points and patients tested; with columns meaning the number of attributes or more specifically features that will determine what exactly affects the model. The dataset was definitely large enough to feed the model as it contained 768 datapoints. This was when I was introduced to the term "Exploratory Data Analysis". It was something I did not fully attempt in this project as I have yet to fully grasp it, however looking at some inspirations like the notebook from Ahmet Can Karaoglan, this part uses Matplotlib and Seaborn libraries to find correlations and skewness in the data for example.

## Data Preprocessing

I managed to learn from an uncle who works in the Machine Learning field that this part is the most important one in the lifecycle of a model. It takes the longest usually in any major company because what you input into your model is what you end up obtaining so if you put garbage in you will get garbage out. Here in this case I was introduced to and also managed to implement some necessary data cleansing techniques. For instance, I had to figure out how to view the number of 0 values in the data and replace them, starting with replacing them with NaN (Not a Number) values. The NaN values were then replaced with the means of each of the respective columns.

### Feature Scaling

Under the data preprocessing stage I learnt of something called feature scaling which involves using either standardization or normalization. These are statistical methods used to make sure that no feature affects the model's outcome more than the rest removing bias. In this case I used the StandardScaler() function which involves making the mean 0 and standard deviation 1 for all attributes. This function carries out the following formula: (X-μ)/σ which subtracts the mean from the observation and divides it by the std.


## Model Testing and Deployment of Browser

We then split the model into testing and training data using the train_test_split function. This allows us to to train the model on 80 percent of the data then testing it on unseen data using the remaining 20 percent. Then in order for the model to be satisfactory, the right algorithm will have to be used. Now, I wouldn't say I was introduced to every algorithm out there, however out of the ones that I do know I decided to experiment on. So I went with 3 different ones... The SVM (Support Vector Machine), Random-Forest Classifier and the classic Logistic Regression which are all used in determining a binary classification problem. After testing the above-mentioned algorithms, I found out that without finetuning the best performing algorithm out of the three was the Logistic Regression. I also consolidated this information when introduced to the cross_val_score function which carries out a stratified k-fold validation technique splitting each batch/ fold of data into both training and testing data at some point which is much more accurate than the normal train_test_split. We managed to achieve a 77.5% accuracy which for a first-time project I am pretty happy with. 

![Test Image 2]("C:\Users\ramah\Desktop\Jacobs University Files\Projects\DiabetesPredictorProject\LogisticRegression.png")

Using the library known as Streamlit I managed to make the browser that allows a User to input the values they have for each of the Feature columns with a predict button found at the bottom that allows the user to see the outcome; whether "Diabetic" or "Non-diabetic".

## Problems I faced

Unfortunately I ran into a problem which I spent ages trying to solve, although my model was working fine predicting Diabetic outcomes correctly with an accuracy of 77.5% ; whenever I input data manually it would always give a "Diabetic" result. It also shows that the ML model is 88% percent confident with the Non-diabetic results which is even more confusing! If anyone could reach out to me to help me solve this it would be epic.

## Improvements

For my next project I should focus more on doing EDA- a more in-depth analysis of the data given using the Seaborn library. 
In the Data Preprocessing part I could use my knowledge in upper and lower quartile and determine the interquartile range to fully remove any outliers using the LocalOutlierFactor. In addition, I could use doing some feature engineering such as one-hot encoding and/or binning for next time. In general, I should spend more time customizing and editing the data to be better suited for the model. When it comes to algorithms I can definitely include many more. There is one I learnt for example that is called XGBBooster, then once determining the accuracy score we can do some finetuning to further improve the accuracy of the model.
