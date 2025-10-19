# Amazon Fine Food Reviews - Sentiment Analysis

This project performs sentiment analysis on the Amazon Fine Food Reviews dataset using both **VADER (Valence Aware Dictionary and sEntiment Reasoner)** and **RoBERTa (Transformer-based)** models. The goal is to compare the performance of these two different approaches to sentiment analysis.

## 📁 Project Structure

- **Data Loading & Exploration**: Loading the Amazon Fine Food Reviews dataset and performing initial exploratory data analysis
- **Text Preprocessing**: Tokenization, part-of-speech tagging, and named entity recognition using NLTK
- **VADER Sentiment Analysis**: Using the lexicon-based VADER model for sentiment scoring
- **RoBERTa Sentiment Analysis**: Using the transformer-based RoBERTa model for more contextual sentiment analysis
- **Comparative Analysis**: Visualizing and comparing results from both models

## 🛠️ Technologies Used

- **Python 3.10.12**
- **Libraries**:
  - `pandas` - Data manipulation and analysis
  - `numpy` - Numerical computing
  - `matplotlib` & `seaborn` - Data visualization
  - `nltk` - Natural Language Toolkit for text processing
  - `transformers` - HuggingFace library for transformer models
  - `scipy` - Scientific computing

## 📊 Dataset

The project uses the **Amazon Fine Food Reviews** dataset containing:
- **568,454 reviews** of fine foods from Amazon
- **10 columns** including ProductId, UserId, Score, Summary, and Text
- **Score ratings** from 1 to 5 stars

## 🔍 Key Features

### 1. **VADER Analysis**
- Lexicon-based sentiment analysis
- Specialized for social media and short texts
- Provides compound, positive, negative, and neutral scores
- Fast but doesn't account for word relationships

### 2. **RoBERTa Analysis**
- Transformer-based pre-trained model
- Accounts for context and relationships between words
- More accurate but computationally intensive
- Provides probability scores for negative, neutral, and positive sentiments

### 3. **Comparative Visualization**
- Bar plots comparing sentiment scores across different star ratings
- Analysis of how both models perform across the rating spectrum

## 📈 Results

The project demonstrates:
- How traditional lexicon-based approaches (VADER) compare with modern transformer models (RoBERTa)
- The relationship between explicit star ratings and computed sentiment scores
- Visualizations showing sentiment distribution across different review scores

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn nltk transformers scipy tqdm
