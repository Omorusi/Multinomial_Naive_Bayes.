# Multinomial Naive Bayes Model for Sentiment Analysis
This project demonstrates the application of the Multinomial Naive Bayes model for sentiment analysis on a Twitter dataset. The dataset consists of text comments associated with various topics, with the goal of predicting the emotional sentiment behind each comment (e.g., Positive, Negative, Neutral, or Irrelevant).

 # Overview
The project focuses on building a sentiment analysis pipeline using Multinomial Naive Bayes to classify Twitter comments based on their emotional content. The dataset contains textual data that is transformed into numerical format through CountVectorizer and TfidfVectorizer, followed by training the model to predict emotional categories like Positive, Negative, Neutral, and Irrelevant.

 # Technologies Used
Python: The programming language used for model development.
Scikit-learn: For machine learning algorithms and utilities like train_test_split, CountVectorizer, and MultinomialNB.
Matplotlib & Seaborn: For data visualization, including generating pie charts and confusion matrices.
Pandas: For data manipulation and cleaning.
Data Collection
The dataset used in this project is a CSV file, twitter_training.csv, containing tweets related to various topics and their corresponding emotional sentiment (Positive, Negative, Neutral, or Irrelevant). The data was loaded into a pandas DataFrame for preprocessing, which includes renaming columns, handling missing values, and preparing the dataset for model training.

 # Data Preprocessing
The following steps were performed during the preprocessing phase:

Renaming columns: To ensure clear representation of the data, column names were updated.
![image alt](!https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20124153.png?raw=true
)
Handling missing values: Empty comments were removed from the dataset.
![image alt](https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20124326.png?raw=true)
Text vectorization: Raw text comments were converted into numerical features using the CountVectorizer and TfidfVectorizer.
![image alt](https://github.com/Omorusi/Multinomial_Naive_Bayes./blob/main/Screenshot%202025-03-03%20124408.png?raw=true)
Model Training
The sentiment analysis model was trained using the Multinomial Naive Bayes classifier, a commonly used model for text classification tasks. The dataset was split into training and testing sets, and the model was trained on the training data. The model was then evaluated on the test data to assess its performance.

python
Copy
Edit
# Model Training
from sklearn.naive_bayes import MultinomialNB
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X_vectorized, y, test_size=0.2, random_state=42)
model = MultinomialNB()
model.fit(X_train, y_train)
Model Evaluation
The performance of the Multinomial Naive Bayes model was evaluated using several metrics, including accuracy, precision, recall, and F1-score. The classification report and confusion matrix were generated to assess the model's performance in classifying comments into the emotional categories.

Accuracy: 76%
Precision, Recall, and F1-Score: Various metrics for each sentiment category.
python
Copy
Edit
from sklearn.metrics import classification_report
print(classification_report(y_test, y_pred))
Visualizations
Sentiment Distribution: A pie chart was generated to visualize the distribution of sentiments in the dataset.

Confusion Matrix: A heatmap of the confusion matrix was created to visualize how well the model is performing in terms of true and predicted sentiment labels.

python
Copy
Edit
from sklearn.metrics import confusion_matrix
import seaborn as sns

mat = confusion_matrix(y_test, y_pred)
sns.heatmap(mat.T, annot=True, fmt='d', cmap="Blues", xticklabels=labels, yticklabels=labels)
Results
The Multinomial Naive Bayes model achieved an accuracy of 76% on the test set. The model demonstrated good performance in categorizing comments into the correct sentiment labels, with the best performance for Negative sentiment.

Conclusion
The Multinomial Naive Bayes model proves to be an effective method for text classification in sentiment analysis tasks. By transforming text into numerical features and applying the Naive Bayes algorithm, we can accurately predict the emotional sentiment of tweets. This project highlights the power of machine learning in understanding social media content and can be extended for larger datasets or used in real-time applications.

