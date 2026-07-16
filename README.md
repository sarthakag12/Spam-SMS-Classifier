# Spam SMS Classifier

A Natural Language Processing (NLP) application that classifies SMS messages as **Spam** or **Not Spam** using text preprocessing, TF-IDF vectorization, and a machine learning classification model.

The project includes a Streamlit web application that allows users to enter an SMS message and receive a real-time prediction.

## Features

- Classifies SMS messages as Spam or Not Spam
- Text preprocessing using:
  - Tokenization
  - Stopword removal
  - Punctuation removal
  - Stemming
- Converts text into numerical features using TF-IDF
- Uses a trained machine learning model for classification
- Provides an interactive Streamlit web interface
- Supports real-time predictions

## Machine Learning Pipeline

```text
SMS Message
     ↓
Text Preprocessing
     ↓
Tokenization
     ↓
Stopword & Punctuation Removal
     ↓
Stemming
     ↓
TF-IDF Vectorization
     ↓
Machine Learning Model
     ↓
Spam / Not Spam Prediction
```

## Tech Stack
* Python
* Pandas
* NumPy
* NLTK
* Scikit-learn
* Streamlit
* Pickle

## Project Structure
```
Spam-SMS-Classifier/
│
├── app.py                    # Streamlit application
├── SMS_Spam_Classifier.ipynb # Model training and analysis
├── spam.csv                  # Dataset
├── model.pkl                 # Trained machine learning model
├── vectorizer.pkl            # Trained TF-IDF vectorizer
├── requirements.txt          # Project dependencies
└── README.md
```
## How It Works

1. Text Preprocessing

The input SMS is processed through the following steps:

- Convert text to lowercase
- Tokenize the text
- Remove non-alphanumeric characters
- Remove English stopwords
- Apply Porter Stemming

2. Feature Extraction

The preprocessed text is transformed into numerical features using a trained TF-IDF vectorizer.

3. Classification

The TF-IDF representation is passed to a trained machine learning model that predicts whether the message is:

* Spam
* Not Spam

## Installation

1. Clone the repository:

```
git clone <your-repository-url>
cd Spam-SMS-Classifier
```

2. Install the required dependencies:

```
pip install -r requirements.txt
```

3. Download the required NLTK resources:

```
import nltk

nltk.download('punkt')
nltk.download('stopwords')
```
4. Run the Application

Start the Streamlit application:
```
streamlit run app.py
```

The application will open in your browser.
