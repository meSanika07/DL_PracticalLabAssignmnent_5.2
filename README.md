# 🧪 Experiment 5.2: Sequence Text Prediction using LSTM

## 🎯 Objective
To generate the next words based on a given input sequence using Long Short-Term Memory (LSTM) neural networks.

---

## 📁 Dataset Used
**Primary Dataset:**  
- News Headline Dataset (`News_Headline.csv`)

**Other Suggested Datasets for Experimentation:**
- Shakespeare’s Text (TFDS)
- Pride and Prejudice – Jane Austen (Project Gutenberg)
- Harry Potter Books Dataset
- Cornell Movie Dialogs
- Reddit Jokes Dataset
- Taylor Swift / Beatles Lyrics
- Wikipedia Articles Dump
- Quora Question Pairs
- English Proverbs

---

## 📊 Expected Outcome
- Auto-generated news headlines based on a seed input
- Training accuracy and loss graphs
- 
---

## 🔧 Tech Stack
- Python 3.x
- TensorFlow / Keras
- Pandas, NumPy
- Matplotlib, Seaborn

---

## 📌 Steps Followed

### 1. **Data Preprocessing**
- Loaded `News_Headline.csv`
- Extracted `headlines` column
- Limited dataset to first 500 headlines for faster experimentation

### 2. **Tokenization & Sequence Creation**
- Used Keras `Tokenizer` to convert text to sequences
- Generated n-gram sequences
- Padded sequences to maximum length of 15

### 3. **Predictor/Label Split**
- Split sequences into predictors (`X`) and labels (`y`)
- One-hot encoded the labels using `to_categorical`

### 4. **Model Architecture**
```python
Sequential Model:
- Embedding Layer (output_dim=80)
- Dropout (0.2)
- Bidirectional LSTM (90 units)
- Dense Layer (softmax over total_words)
```
- Optimizer: `Adam`
- Loss: `categorical_crossentropy`
- Metric: `accuracy`

### 5. **Training**
- Trained for 100 epochs
- Final accuracy achieved: **~98%**

### 6. **Performance Visualization**
- Accuracy and Loss plotted per epoch:  
**Training Accuracy:** ![Training Accuracy](https://github.com/user-attachments/assets/d31adcb2-c961-4a7f-b83a-e593cddc8357) **Training Loss:** ![Training Loss](https://github.com/user-attachments/assets/07b076f9-4dab-4534-b372-1240e6ff3631)

### 7. **Text Prediction Demo**
Tested predictions on the following seed phrases:


---
