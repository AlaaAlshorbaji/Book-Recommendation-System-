# 📚 Book Recommendation System using Collaborative Filtering

This repository contains a recommendation system that predicts user ratings for books using collaborative filtering techniques implemented via the Surprise library. The notebook guides you through the entire workflow — from loading the dataset to evaluating predictions — with the aim of recommending books tailored to user preferences.

## 🎯 Objective

The goal of this project is to recommend books to users by analyzing their past ratings and comparing them with similar users using matrix factorization (SVD).

This tutorial helps you understand:
- How recommendation systems function
- How to use collaborative filtering (SVD) with the Surprise library
- How to evaluate models using RMSE and MAE

## 📘 Dataset

The dataset used contains:
- `user_id`: Unique identifier for each user
- `book_title`: Title of the book rated
- `rating`: User-assigned rating

Data has been preprocessed and filtered to retain:
- Active users who rated many books
- Popular books that received many ratings
## 📁 File Structure

The project is implemented entirely in one notebook:


This notebook is organized into the following sections:

---

### 1. 📚 Importing Libraries

Imports essential libraries:
- `pandas`, `numpy` – for data handling
- `matplotlib`, `seaborn` – for visualization
- `surprise` – for building the recommendation model
- `warnings` – to suppress unnecessary output

---

### 2. 📥 Loading and Merging Data

- Reads the dataset containing book ratings and titles.
- Merges relevant columns such as `user_id`, `book_title`, and `rating`.
- Displays the head and shape of the dataset to understand its structure.

---

### 3. 🔍 Data Exploration and Filtering

- Visualizes the most frequently rated books using bar plots.
- Analyzes rating distributions.
- Filters:
  - Users who have rated more than a certain number of books.
  - Books that have been rated frequently.
- Merges filtered results to create a more meaningful subset for training.

---

### 4. 🧼 Data Preprocessing for Surprise

- Uses the `Reader` and `Dataset` classes from `surprise`.
- Prepares the final `ratings_filtered` DataFrame with columns: `user_id`, `book_title`, `rating`.

---

### 5. 🧠 Model Building with SVD

- Splits the data using `train_test_split`.
- Builds a collaborative filtering model using `SVD`.
- Trains the model on the training set.

---

### 6. 📈 Model Evaluation

- Evaluates the model using RMSE and MAE.
- Uses `accuracy` module from Surprise to compare predictions to actual ratings.

---

### 7. 🔮 Making Predictions

- Predicts a rating for a specific book by a specific user.
- Syntax: `model.predict(user_id, book_title)`
- Displays estimated rating (`est`) and other prediction metadata.

---

This structure gives a complete pipeline from raw data to personalized book recommendations.
## ⚙️ Getting Started

This notebook is built using Python and Jupyter. You can run it on your local machine or on Google Colab.

---

### 📋 1. Prerequisites

Make sure you have the following libraries installed:


pip install pandas numpy matplotlib seaborn scikit-surprise
▶️ 2. Running the Notebook
🖥️ Run Locally:
Launch Jupyter Notebook:


jupyter notebook Rrcommendation_System.ipynb
Execute each cell in order.

🌐 Run on Google Colab:
Open Google Colab

Upload the notebook file.

Make sure to install surprise:


!pip install scikit-surprise
Run the cells sequentially.

🖼️ 3. Output
Visualizations of most rated books and rating distributions.

Model training and evaluation using RMSE and MAE.

Personalized rating predictions (e.g., estimating a user’s potential rating for a book).

## 👨‍💻 Author

**Alaa Shorbaji**  
Artificial Intelligence Instructor  
Machine Learning & NLP Researcher  

---

## 📜 License

This project is licensed under the **MIT License**.

You are free to:

- ✅ Use and share the code for personal, academic, or commercial purposes.  
- ✅ Modify, distribute, and build upon the code with proper credit.

You must:

- ❗ Provide appropriate attribution to the original author.  
- ❗ Include this license notice in any copies or substantial portions of the project.

> **Disclaimer:** This notebook uses open-source libraries and datasets. It does not claim ownership of any third-party resources included or referenced within the notebook. Please respect the licenses of any external data or tools used.

---

