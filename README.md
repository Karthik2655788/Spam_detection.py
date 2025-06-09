# Spam_detection.py


# 📨 Simple Spam Classifier Using Naive Bayes

This is a minimal example of a spam detection system using Python's `scikit-learn` library. It demonstrates the use of the **Multinomial Naive Bayes** classifier along with **CountVectorizer** to convert text into numeric form for classification.

## 🚀 Features

* Text preprocessing with `CountVectorizer`
* Classification using `MultinomialNB`
* Tiny sample dataset for demonstration
* Easy to extend with more data or preprocessing techniques

## 🛠️ Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/spam-classifier.git
cd spam-classifier
```

2. Install the required dependencies:

```bash
pip install scikit-learn
```

## 📄 Code Overview

```python
from sklearn.naive_bayes import MultinomialNB
from sklearn.feature_extraction.text import CountVectorizer

# Sample data
texts = ["Win a prize", "Meeting at 10", "Free lottery", "Project update"]
labels = [1, 0, 1, 0]  # 1 = spam, 0 = not spam

# Convert text to numeric vectors
vectorizer = CountVectorizer()
X = vectorizer.fit_transform(texts)

# Train model
model = MultinomialNB()
model.fit(X, labels)

# Predict on new message
test = vectorizer.transform(["Free meeting"])
print(model.predict(test))  # Output: [1] for spam, [0] for not spam
```

## 📊 Example Output

```bash
[1]
```

The model predicts the message `"Free meeting"` as **spam** based on learned patterns.

## 📈 Future Improvements

* Add more training samples
* Use `TfidfVectorizer` for better weighting
* Integrate with a simple Flask API or UI
* Evaluate model using metrics like accuracy, precision, recall

## 📚 Requirements

* Python 3.6+
* `scikit-learn`




