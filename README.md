📰 Fake News Detection using Machine Learning

This project implements a Fake News Detection system using Natural Language Processing (NLP) and Machine Learning. The model analyzes news article titles and predicts whether the news is Real or Fake.

The system uses text preprocessing, stemming, TF-IDF vectorization, and Logistic Regression to classify news articles.

📂 Dataset

The model uses the WELFake Dataset, which contains labeled news articles.

Dataset Features
Column	Description
title	Title of the news article
text	Full content of the news article
label	Target variable (0 = Real News, 1 = Fake News)
⚙️ Technologies Used
Python
Pandas
NumPy
NLTK
Scikit-learn
Regex (re)
TF-IDF Vectorizer
Logistic Regression
📊 Project Workflow

The project follows the following steps:

1️⃣ Import Libraries

Libraries for data processing, NLP, and machine learning are imported.

2️⃣ Load Dataset

The dataset is loaded using Pandas.

news_dataset = pd.read_csv('WELFake_Dataset.csv')
3️⃣ Data Preprocessing
Handling missing values
Cleaning text
Removing special characters
Converting text to lowercase
4️⃣ Text Stemming

Stemming reduces words to their root form using Porter Stemmer.

Example:

playing → play
running → run
port_stem = PorterStemmer()
5️⃣ Stopword Removal

Common English words like "the", "is", "and" are removed because they do not contribute to meaning.

6️⃣ Text Vectorization

The cleaned text is converted into numerical features using TF-IDF Vectorizer.

vectorizer = TfidfVectorizer()
X = vectorizer.fit_transform(X)
7️⃣ Train-Test Split

The dataset is split into training and testing data.

train_test_split(X, Y, test_size=0.2)
80% Training Data
20% Testing Data
8️⃣ Model Training

A Logistic Regression model is used for classification.

model = LogisticRegression()
model.fit(X_train, Y_train)
9️⃣ Model Evaluation

Accuracy is calculated for both training and test datasets.

accuracy_score()
📈 Results

The model predicts whether news is Real or Fake based on the input text.

Example prediction:

if prediction[0] == 0:
    print("The news is Real")
else:
    print("The news is Fake")
🚀 How to Run the Project
1️⃣ Clone the repository
git clone https://github.com/yourusername/Fake-News-Detection.git
2️⃣ Install dependencies
pip install pandas numpy scikit-learn nltk tqdm
3️⃣ Download NLTK stopwords
import nltk
nltk.download('stopwords')
4️⃣ Run the Notebook

Open and run:

Fake_News_Detection.ipynb
📌 Project Features

✔ Text preprocessing using NLP
✔ Stopword removal
✔ Word stemming
✔ TF-IDF feature extraction
✔ Logistic Regression classification
✔ Real vs Fake news prediction

🔮 Future Improvements
Use Deep Learning models (LSTM / BERT)
Use full article text instead of only titles
Deploy as a web application
Improve preprocessing pipeline
