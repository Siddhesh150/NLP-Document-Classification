
# 📄 Document Classification using NLP


This project implements a **Natural Language Processing (NLP)** based document classification system using Machine Learning and TF-IDF feature extraction.

The system trains multiple models on the 20 Newsgroups dataset and selects the best-performing model for predictions.

It includes:

* 🧠 Model training script (Naive Bayes & Logistic Regression)
* 💾 Automatic best-model selection
* 📦 Model serialization using Pickle
* 💻 Command-line prediction interface
* 🌐 Streamlit web application (optional UI)

---

## 🚀 Project Overview

This project performs **multi-class text classification** using:

* TF-IDF feature extraction
* Scikit-learn
* Streamlit (for web interface)

Two models are trained and compared:

* Multinomial Naive Bayes
* Logistic Regression

The model with the higher accuracy is automatically saved and used for predictions.

---

## 🛠️ Tech Stack

* Python
* NumPy
* Scikit-learn
* Streamlit
* Pickle

---

## 📂 Project Structure

```
├── documentclassification.py            # Model training & evaluation script
├── app.py              # Streamlit web application
├── model.pkl           # Saved best ML model
├── vectorizer.pkl      # Saved TF-IDF vectorizer
├── README.md           # Project documentation
```

---

## ⚙️ How It Works

### 1️⃣ Load Dataset

The program loads the complete 20 Newsgroups dataset including:

* Text documents
* Target labels
* Category names

### 2️⃣ Train-Test Split

The dataset is split:

* 80% Training
* 20% Testing

### 3️⃣ Feature Extraction

Text data is converted into numerical form using:

* **TF-IDF Vectorizer**
* English stopword removal
* Maximum 10,000 features

### 4️⃣ Model Training

Two models are trained:

* Multinomial Naive Bayes
* Logistic Regression (max_iter=1000)

### 5️⃣ Model Evaluation

Models are evaluated using:

* Accuracy score
* Classification report (precision, recall, F1-score)

### 6️⃣ Best Model Selection

The model with higher accuracy is automatically selected and saved as:

```
model.pkl
vectorizer.pkl
```

### 7️⃣ Prediction System

Users can:

* Enter text in the terminal
* Type `exit` to quit
* Receive predicted category instantly

---

## 📊 Example Output

```
Naive Bayes Accuracy: 0.83
Logistic Regression Accuracy: 0.91

Best model saved successfully!
```

Example Prediction:

```
Enter your document text:
NASA launched a satellite into orbit.

Predicted Category: sci.space
```

---

## 🖥️ Running the Training Script

```bash
python train.py
```

After execution:

* The best model will be saved
* You can start making predictions immediately

---

## 🌐 Running the Streamlit Web App 

If you are using the Streamlit interface:

```bash
streamlit run app.py
```

Then open:

```
http://localhost:8501
```

Features in the web app:

* Text input area
* Predicted category display
* Confidence score
* Top 10 probability bar chart
* Modern dark UI theme

---

## 📈 Model Performance

Typically:

* Logistic Regression performs better than Naive Bayes
* Accuracy ranges between **88%–92%** depending on split

---

## 🔮 Future Improvements

* Add deep learning models (LSTM / BERT)
* Add confusion matrix visualization
* Allow file uploads (.txt)
* Deploy to cloud (Streamlit Cloud / Render / AWS)
* Add REST API version using Flask or FastAPI

---

## 📜 License

This project is created for educational purposes.
Free to use and modify.

---

## 👨‍💻 Author

**Krishna Parashar**
Machine Learning & AI Enthusiast 🚀



