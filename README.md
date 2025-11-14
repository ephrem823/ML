# 📘 Amharic Question-Answering System (TF-IDF Based)

A simple Amharic Question-Answering (QA) system that uses TF-IDF and cosine similarity to match a user question with the closest question from a dataset and return its correct answer.

This project demonstrates basic NLP techniques for Amharic using a SQuAD-style JSON dataset.

---

 🚀 Features
- Load Amharic QA dataset (JSON)
- Clean and tokenize Amharic text
- Remove Amharic stopwords
- Convert text to TF-IDF vectors
- Compare similarity using cosine distance
- Return the best matching answer

---

📂 Project Structure
```
├── haramaya_amharic_qa.json        # Input dataset
├── amharic_qa.py                   # Main QA script
└── README.md                       # Project documentation
```

---
 🧠 How It Works

1. Dataset Loading  
The system loads `haramaya_amharic_qa.json`, which contains:
- contexts  
- questions  
- answers  

Each question–answer pair is extracted for processing.

---

2. Text Cleaning  
We remove:
- punctuation  
- English letters  
- numbers  

This ensures only clean Amharic words are left.

---

3. Tokenization & Stopwords  
Text is split into words using `.split()` and common Amharic words like “እና”, “ወይም”, “የ” are removed.

---

4. TF-IDF Vectorization  
Every question is converted into a numeric vector using scikit-learn's `TfidfVectorizer`.  
Higher values = more important words in that question.

---

5. Question Matching  
When you type a new question:
1. It is cleaned and vectorized  
2. Compared with all dataset questions  
3. Cosine similarity finds the closest match  
4. The matched answer from the dataset is returned  

---

## 💻 Example Run
```
🗣️ የእርስዎ ጥያቄ ያስገቡ፦ ሐረማያ ዩኒቨርሲቲ መቼ ተመሰረተ?

🤔 ተመሳሳይ ጥያቄ: ሐረማያ ዩኒቨርሲቲ መቼ ተመሰረተ?
✅ መልስ: በ1950ዎቹ መጀመሪያ
```


## 📌 Author
Created by **ephrem** for Amharic NLP learning and experimentation 🎓✨
