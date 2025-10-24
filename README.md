# Ex-1-Developing-AI-Agent-with-PEAS-Description
### Name: Deekshitha K

### Register Number: 2305002005

### Aim:
To find the PEAS description for the given AI problem and develop an AI agent.

### Theory :
PEAS stands for:
'''
P-Performance measure

E-Environment

A-Actuators

S-Sensors
'''

It’s a framework used to define the task environment for an AI agent clearly.

### Pick an AI Problem

```

1. Self-driving car

2. Chess playing agent

3. Vacuum cleaning robot

4. Email spam filter

5. Personal assistant (like Siri or Alexa)
```

### E-mail spam filter
### Algorithm:
Step 1: Collect a dataset of emails labeled as Spam or Ham (Not Spam).

Step 2: Preprocess the email text by converting to lowercase, removing punctuation, numbers, and stopwords.

Step 3: Tokenize the text by splitting each email into individual words.

Step 4: Extract features using techniques like Bag of Words or TF-IDF, converting text into numerical vectors.

Step 5: Split the dataset into Training Set and Testing Set (e.g., 80% training, 20% testing).

Step 6: Select a classification algorithm, commonly Naive Bayes for spam filtering.

Step 7: Train the model using the training dataset so it learns patterns of spam and ham emails.

Step 8: Test the model on the testing dataset and predict whether emails are Spam or Ham.

Step 9: Evaluate the model’s performance using accuracy, precision, recall, and F1-score.

Step 10: Deploy the model in an email system to automatically filter incoming emails.

Step 11: Continuously update and retrain the model with new data for better accuracy.

### Program:
```
# Basic Email Spam Filter in Python

from sklearn.feature_extraction.text import CountVectorizer
from sklearn.naive_bayes import MultinomialNB

# Step 1: Sample Dataset (for demo)
emails = [
    "Win money now!!!", 
    "Lowest price for medicines", 
    "Hi, how are you?", 
    "Meeting tomorrow at 10am", 
    "Congratulations, you won a lottery", 
    "Reminder: project submission"
]
labels = ["spam", "spam", "ham", "ham", "spam", "ham"]

# Step 2: Convert text to numbers
vectorizer = CountVectorizer()
X = vectorizer.fit_transform(emails)

# Step 3: Train Naive Bayes classifier
model = MultinomialNB()
model.fit(X, labels)

# Step 4: Test new email
test_email = ["Get cheap loans now"]
test_vector = vectorizer.transform(test_email)
prediction = model.predict(test_vector)

print("Email:", test_email[0])
print("Prediction:", prediction[0])
```
### Sample Output:

<img width="491" height="67" alt="image" src="https://github.com/user-attachments/assets/5b85651b-f9e3-4833-bcde-ce94c5f6647d" />


### Result:
Thus, the program for Email Spam Filter was implemented and executed successfully.
