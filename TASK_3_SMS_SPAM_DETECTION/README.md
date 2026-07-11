#  SMS Spam Detection using Machine Learning

A machine learning project that classifies SMS messages as **Spam** or **Ham (Legitimate)** using Natural Language Processing (NLP) techniques and supervised learning algorithms.

This project was developed as **Task 3** for the **CodSoft Machine Learning Internship**.

---

##  Project Overview

Spam messages have become increasingly common and often contain advertisements, phishing attempts, or fraudulent links. The goal of this project is to build a machine learning model capable of automatically identifying whether an SMS message is spam or legitimate.

The workflow includes:

- Data preprocessing
- Text cleaning
- Feature extraction using TF-IDF
- Training multiple machine learning models
- Model evaluation and comparison
- Saving the best-performing model for future predictions

---

##  Dataset

The project uses the **SMS Spam Collection Dataset**, which contains thousands of labeled SMS messages.

Each message is categorized as:

- **Ham** → Legitimate message
- **Spam** → Unwanted or promotional message

Example:

| Label | Message |
|-------|---------|
| Ham | Hey, are we still meeting today? |
| Spam | Congratulations! You've won a FREE vacation. Click here to claim now! |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- NLTK
- Scikit-learn
- Joblib

---

## 📚 Machine Learning Workflow

### 1. Data Loading

- Load the dataset
- Remove unnecessary columns
- Rename columns for better readability

### 2. Data Cleaning

- Remove duplicate messages
- Handle missing values
- Convert labels into numerical format

### 3. Text Preprocessing

The SMS messages are cleaned using NLP techniques:

- Convert text to lowercase
- Remove punctuation
- Remove stopwords
- Apply Porter Stemming

### 4. Feature Extraction

The cleaned messages are converted into numerical vectors using:

- **TF-IDF Vectorization**

### 5. Model Training

The following machine learning algorithms were trained and compared:

- Multinomial Naive Bayes
- Logistic Regression
- Linear Support Vector Machine (Linear SVM)

### 6. Model Evaluation

Each model is evaluated using:

- Accuracy Score
- Classification Report
- Confusion Matrix

The best-performing model is then saved for future predictions.

---

## 📊 Project Structure

```
SMS-Spam-Detection/
│
├── spam.csv
├── Spam_SMS_Detection.ipynb
├── README.md
├── requirements.txt
│
├── models/
│   ├── spam_model.pkl
│   └── tfidf_vectorizer.pkl
│
└── images/
    └── model_comparison.png
```

---

##  Results

Three different machine learning models were trained and compared.

| Model | Purpose |
|---------|----------|
| Multinomial Naive Bayes | Baseline text classification model |
| Logistic Regression | Linear classifier with strong performance |
| Linear SVM | High-performance classifier for sparse text data |

The model with the highest accuracy was selected and saved for deployment.

---

##  Predicting New Messages

Example:

```python
predict_sms("Congratulations! You have won ₹50,000. Click here to claim.")
```

Output:

```
Spam
```

Example:

```python
predict_sms("Hey, let's meet at 5 PM.")
```

Output:

```
Ham
```

---

##  How to Run

### Clone the repository

```bash
git clone https://github.com/yourusername/codsoft_tasks.git
```

### Navigate to the project

```bash
cd codsoft_tasks
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```
Spam_SMS_Detection.ipynb
```

Run all cells to train and evaluate the models.

---

##  Future Improvements

- Use Word2Vec embeddings
- Experiment with BERT-based text classification
- Hyperparameter tuning
- Deploy the model using Flask or Streamlit
- Build a simple web interface for real-time SMS prediction

---

## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

- Natural Language Processing (NLP)
- Text preprocessing techniques
- TF-IDF feature extraction
- Machine learning model training
- Model evaluation and comparison
- Saving and loading trained models
- Building an end-to-end text classification pipeline

---

##  Acknowledgements

- CodSoft Machine Learning Internship
- UCI SMS Spam Collection Dataset
- Scikit-learn Documentation
- NLTK Documentation

---

##  License

This project is intended for educational and learning purposes as part of the CodSoft Machine Learning Internship.

## Author

Amol Kainthola
