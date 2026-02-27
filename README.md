📘 NLP Text Representation Techniques

This project demonstrates fundamental Natural Language Processing (NLP) techniques for converting text into numerical representations that machine learning models can understand.

🚀 Overview

In NLP, raw text cannot be directly used by machine learning models. This project explores different methods to transform text into vectors:

One-Hot Encoding

Bag of Words (BoW)

N-grams

TF-IDF (Term Frequency – Inverse Document Frequency)

📂 Project Structure
nlp02.ipynb   # Jupyter Notebook with implementation
README.md     # Project documentation
🧠 Concepts Covered
1. One-Hot Encoding

Converts each word into a binary vector.

Each word is represented by a vector where only one index is 1 and the rest are 0.

Example:

Word → Vector
cat → [1, 0, 0]
dog → [0, 1, 0]
bat → [0, 0, 1]
2. Bag of Words (BoW)

Represents text based on word frequency.

Ignores grammar and word order.

Key Idea:

Count how many times each word appears in a document.

3. N-grams

Captures sequences of words.

Helps preserve some context.

Types:

Unigram → Single words

Bigram → Pair of words

Trigram → Three words

Example:

"I love NLP"
Bigrams → ["I love", "love NLP"]
4. TF-IDF

Weighs words based on importance.

Reduces the impact of common words like "the", "is".

Formula:

TF-IDF = TF × IDF

TF (Term Frequency): Frequency of word in document

IDF (Inverse Document Frequency): Importance of word across documents

⚙️ Libraries Used

Python

scikit-learn

OneHotEncoder

CountVectorizer

TfidfVectorizer

💻 Implementation Steps

Define a list of text documents

Create a vocabulary from the text

Apply:

One-Hot Encoding manually

Bag of Words using CountVectorizer

N-grams using ngram_range

TF-IDF using TfidfVectorizer

Display vectorized outputs

📊 Example Workflow
from sklearn.feature_extraction.text import CountVectorizer

cv = CountVectorizer()
X = cv.fit_transform(documents)

print(cv.get_feature_names_out())
print(X.toarray())
🎯 Use Cases

Text Classification

Sentiment Analysis

Chatbots

Search Engines

Recommendation Systems

🔥 Key Takeaways

Text must be converted into numbers for ML models.

BoW is simple but loses context.

N-grams improve context understanding.

TF-IDF helps focus on important words.

🛠️ Future Improvements

Add Word Embeddings (Word2Vec, GloVe)

Implement Transformers (BERT, GPT)

Apply on real-world datasets

👨‍💻 Author

Yousuf Midya
B.Tech CSE (AI & ML)
