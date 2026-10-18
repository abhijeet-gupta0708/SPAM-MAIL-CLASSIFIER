# 📩 SMS Spam Classifier

A Machine Learning and Natural Language Processing (NLP) project that classifies SMS messages as **Spam** or **Not Spam (Ham)** using text preprocessing, TF-IDF vectorization, and a Multinomial Naive Bayes classifier.

## 🚀 Overview

The SMS Spam Classifier analyzes the content of a text message and predicts whether it is spam or a legitimate message. The project includes data preprocessing, exploratory data analysis, model training, evaluation, and an interactive web application built with Streamlit.

## ✨ Features

- **Spam Detection:** Classifies messages as Spam or Not Spam.
- **Text Preprocessing:** Performs lowercasing, tokenization, stopword removal, and stemming.
- **TF-IDF Vectorization:** Converts text into numerical features for machine learning.
- **Machine Learning:** Uses a trained Multinomial Naive Bayes classifier.
- **Interactive Web Interface:** Allows users to enter messages and receive predictions using Streamlit.
- **Model Persistence:** Saves and loads the trained model and vectorizer using Pickle.

## 🛠️ Tech Stack

- **Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Machine Learning:** Scikit-learn
- **Natural Language Processing:** NLTK
- **Visualization:** Matplotlib, Seaborn
- **Web Application:** Streamlit
- **Model Serialization:** Pickle

## 📂 Project Structure

```text
sms-spam-classifier/
│
├── app.py                  # Streamlit web application
├── sms-spam-detection.ipynb # Model training and analysis
├── spam.csv                # SMS dataset
├── model.pkl               # Trained ML model
├── vectorizer.pkl          # Saved TF-IDF vectorizer
├── requirements.txt        # Python dependencies
├── nltk.txt                # NLTK deployment resources
├── setup.sh                # Setup script
├── Procfile                # Deployment configuration
└── README.md               # Project documentation
```

## ⚙️ How It Works

1. **Data Collection:** Loads labeled SMS messages from the dataset.
2. **Data Cleaning:** Removes unnecessary columns, handles duplicate records, and prepares the target labels.
3. **Text Preprocessing:** Converts text to lowercase, tokenizes messages, removes stopwords and punctuation-only tokens, and applies stemming.
4. **Feature Extraction:** Uses TF-IDF to convert processed messages into numerical feature vectors.
5. **Model Training:** Trains and evaluates machine learning classifiers, with Multinomial Naive Bayes used for the saved model.
6. **Prediction:** Processes user input, transforms it using the saved vectorizer, and predicts whether the message is spam.
7. **Result Display:** Shows the prediction through the Streamlit interface.

## 📊 Dataset

The project uses an SMS spam dataset containing messages labeled as:

- **Ham:** Legitimate SMS messages.
- **Spam:** Unwanted or potentially fraudulent messages.

The original dataset contains 5,572 messages. After cleaning and removing duplicate messages, the notebook works with approximately 5,169 records.

## 🧠 Machine Learning Model

The project explores multiple classification algorithms and uses **Multinomial Naive Bayes** for the final saved classifier.

The model uses TF-IDF features to identify patterns associated with spam and legitimate messages.

Evaluation metrics include:

- Accuracy
- Precision
- Confusion Matrix

Performance on the test dataset does not guarantee the same results on new, real-world messages.

## 💻 Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/campusx-official/sms-spam-classifier.git
```

### 2. Navigate to the Project Directory

```bash
cd sms-spam-classifier
```

### 3. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

Ensure that the NLTK resources required by the preprocessing function are installed.

### 5. Run the Application

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal to access the application.

## 📝 Example

**Input:**

```text
Congratulations! You have won a free prize.
Claim your reward now!
```

**Expected Output:** Spam

**Input:**

```text
Hey, are we meeting tomorrow?
```

**Expected Output:** Not Spam

*Note: These are illustrative examples. Actual predictions depend on the trained model.*

## 🔮 Future Improvements

- Improve generalization with more diverse SMS datasets.
- Evaluate the model using cross-validation and additional metrics.
- Prevent data leakage by fitting the vectorizer only on training data.
- Add prediction confidence or probability estimates.
- Deploy the application to a public hosting platform.
- Add support for multilingual spam detection.

## ⚠️ Limitations

- The model is trained on a particular dataset and may not recognize every new spam pattern.
- Legitimate messages may occasionally be classified as spam, and vice versa.
- The model's performance depends on the quality and diversity of its training data.

## 👨‍💻 Author

Developed as a machine learning project to explore Natural Language Processing, text classification, and Streamlit application development.

## 📄 License

Refer to the repository's license information before redistributing or modifying the project.
