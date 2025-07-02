# 🛍️ Amazon Review Intelligence: Sentiment, Helpfulness & BERT Analysis

This project is an end-to-end machine learning and NLP pipeline built to analyze **Amazon product reviews**. It uses both traditional machine learning techniques and modern transformer-based models (BERT) to classify sentiment, predict review helpfulness, and extract actionable insights from e-commerce data.

---

## 📂 Dataset

- The dataset used is a custom **Amazon reviews dataset** (`amazon.csv`).
- It includes:
  - `review_content` – the text of the review  
  - `rating` – the star rating given by the user  
  - `rating_count`, `discounted_price`, `user_id`, `product_category`, etc.

---

## 🎯 Project Objectives

1. 🔍 Perform **sentiment analysis** on review content using BERT  
2. 🏷️ Classify reviews as **POSITIVE**, **NEUTRAL**, or **NEGATIVE**  
3. ✅ Predict whether a review is **helpful** using traditional ML  
4. 🔗 Provide **product recommendations** based on name/category  
5. 🧹 Clean and structure raw Amazon data for ML processing

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas, NumPy, Matplotlib, Seaborn**
- **Scikit-learn**
- **NLTK**
- **Hugging Face Transformers (BERT)**
- **TF-IDF Vectorization**
- **Logistic Regression Classifier**

---

## 🧪 Project Workflow

### 1. 📄 Data Cleaning & Preprocessing
- Dropped missing values
- Cleaned `review_content` using regex and stopwords
- Converted prices and ratings to numeric
- Parsed user IDs

### 2. 🤖 Sentiment Analysis with BERT
- Used pretrained model: `nlptown/bert-base-multilingual-uncased-sentiment`
- Predicted review star ratings
- Mapped stars to:
  - ⭐ 1–2 → NEGATIVE  
  - ⭐ 3 → NEUTRAL  
  - ⭐ 4–5 → POSITIVE

### 3. ✅ Helpfulness Classification
- Rule-based labeling: Helpful = (Rating ≥ 4) AND (Review Length > 50 words)
- Vectorized reviews using **TF-IDF**
- Trained a **Logistic Regression** model to classify helpful vs. non-helpful reviews
- Evaluated with accuracy, F1-score, and classification report

### 4. 🧠 Product Recommendation (Simple)
- Matched products by name similarity and category
- Suggested similar products

### 5. 📊 Visualization
- Confusion matrix
- Review helpfulness distribution
- Prediction previews

---

## 📈 Results & Output

- BERT-based sentiment tags added to every review
- Helpfulness classifier trained and tested with high accuracy
- Example prediction:


---

## 📌 Folder Structure
```bash
.
├── amazon.csv
├── Machine Learning.ipynb
└── README.md
