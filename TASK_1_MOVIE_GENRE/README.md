# Movie Genre Prediction using Machine Learning

## Overview

Choosing a movie often starts with knowing its genre. With thousands of movies being released and cataloged across different platforms, manually assigning genres can become time-consuming and inconsistent. This project aims to automate that process by predicting a movie's genre using only its plot summary.

The model is trained on a large collection of movie descriptions and learns the relationship between the language used in a plot and its corresponding genre. Given a new movie description, the system can predict whether the movie belongs to genres such as Drama, Comedy, Horror, Action, Documentary, Thriller, and many others.

This project was completed as part of the CodSoft Machine Learning Internship.

---

## Problem Statement

Build a machine learning model capable of predicting the genre of a movie based on its textual description.

Since movie plots are unstructured text data, this problem falls under the domain of Natural Language Processing (NLP) and Text Classification.

---

## Dataset Description

The dataset consists of three text files:

### Training Dataset

Format:

ID ::: TITLE ::: GENRE ::: DESCRIPTION

This file contains movie titles, their genres, and plot summaries used for training the model.

### Test Dataset

Format:

ID ::: TITLE ::: DESCRIPTION

This file contains unseen movie descriptions for which the model must predict genres.

### Test Solution Dataset

Format:

ID ::: TITLE ::: GENRE ::: DESCRIPTION

This file contains the actual genres of test movies and is used to evaluate model performance.

---

## Project Workflow

The project follows a complete machine learning pipeline:

### 1. Data Loading

The training and testing datasets are loaded using Pandas and converted into structured DataFrames.

### 2. Data Exploration

Basic exploratory analysis is performed to understand:

* Number of movies
* Number of genres
* Genre distribution
* Missing values
* Dataset dimensions

### 3. Text Preprocessing

Raw movie descriptions contain punctuation, numbers, and unnecessary words that do not contribute significantly to prediction.

The following preprocessing steps are applied:

* Convert text to lowercase
* Remove punctuation and special characters
* Remove stopwords
* Perform lemmatization
* Create cleaned descriptions

Example:

Original:

A young wizard discovers magical powers and joins a mysterious school.

Processed:

young wizard discovers magical power joins mysterious school

### 4. Feature Extraction

Machine learning algorithms cannot understand text directly.

TF-IDF (Term Frequency – Inverse Document Frequency) is used to convert textual descriptions into numerical vectors while preserving the importance of meaningful words.

### 5. Model Training

A Logistic Regression classifier is trained on the TF-IDF features extracted from movie descriptions.

The model learns patterns associated with different genres and uses those patterns for future predictions.

### 6. Model Evaluation

The trained model is evaluated using:

* Accuracy Score
* Precision
* Recall
* F1 Score
* Classification Report
* Confusion Matrix

### 7. Genre Prediction

Once trained, the model can predict genres for previously unseen movie descriptions.

---

## Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* NLTK
* Scikit-learn
* Regular Expressions (re)

### Machine Learning Techniques

* Natural Language Processing (NLP)
* TF-IDF Vectorization
* Logistic Regression
* Text Classification

---

## Project Structure

Movie-Genre-Prediction/

│

├── train_data.txt

├── test_data.txt

├── test_data_solution.txt

├── MOVIE_GENRE.ipynb

├── movie_genre_predictions.csv

├── README.md

│

└── requirements.txt

---

## How to Run the Project

### Clone the Repository

git clone <repository-url>

cd Movie-Genre-Prediction

### Install Dependencies

pip install pandas numpy nltk scikit-learn

### Run Jupyter Notebook

jupyter notebook

Open:

Movie_Genre_Prediction.ipynb

Run all cells sequentially.

---

## Sample Prediction

Input Description:

A retired detective investigates a series of mysterious murders that terrorize a small town.

Predicted Genre:

Thriller

---

## Results

The model successfully learns patterns from movie plot summaries and predicts genres for unseen movies.

Although movie genres often overlap and many movies belong to multiple categories, the model achieves reliable performance using a traditional machine learning approach.

The project demonstrates how NLP techniques can transform raw text into meaningful features that allow machines to perform automated classification tasks.

---

## Future Improvements

Several improvements can further enhance performance:

* Use Linear Support Vector Machines (SVM)
* Hyperparameter tuning
* Use Word2Vec embeddings
* Apply Deep Learning models such as LSTM
* Fine-tune transformer models like BERT
* Support multi-label genre classification

---

## Key Learnings

Through this project, I gained practical experience in:

* Text preprocessing
* Natural Language Processing
* Feature engineering using TF-IDF
* Building machine learning pipelines
* Model evaluation techniques
* Genre classification using textual data

This project helped strengthen my understanding of how machine learning can be applied to real-world text classification problems.

---

## Author

Amol Kainthola
