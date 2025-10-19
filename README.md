# Sentiment Analysis on Amazon Fine Food Reviews

## Overview

This project performs sentiment analysis on the Amazon Fine Food Reviews dataset using Python. It analyzes customer review texts to determine sentiment (positive, negative, or neutral) and correlates these with star ratings. The project uses libraries like Pandas, NLTK, Matplotlib, Seaborn, and the RoBERTa model for sentiment analysis.

## Dataset

- **Source**: [Amazon Fine Food Reviews](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) (Kaggle)
- **Description**: Contains 568,454 reviews of food products sold on Amazon.
- **Key Columns**:
  - `Score`: Star rating (1–5)
  - `Text`: Review text
  - Other columns: `Id`, `ProductId`, `UserId`, `ProfileName`, `HelpfulnessNumerator`, `HelpfulnessDenominator`, `Time`, `Summary`
- **Size**: 568,454 rows, 10 columns

## Features

- **Data Exploration**: Visualizes review distribution by star rating using bar plots.
- **Sentiment Analysis**: Computes sentiment scores using the RoBERTa model.
- **Visualization**: Displays positive sentiment scores (`roberta_pos`) by star rating.

## Requirements

- Python 3.10
- Libraries:
  ```
  pandas
  nltk
  numpy
  matplotlib
  seaborn
  transformers
  ```
- Optional: GPU (e.g., NVIDIA Tesla T4) with CUDA and cuDNN for faster processing

## Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/JedAbidi/Sentiment-Analysis.git
   
   ```

2. **Set Up **:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download Dataset**:
   - Get `Reviews.csv` from [Kaggle](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews).
   - Place it in the project directory or update the file path in the notebook.

## Usage

1. **Run the Notebook**:
   ```bash
   jupyter notebook Sentiment_Analysis_Notebook.ipynb
   ```

2. **Key Steps**:
   - **Load Data**: Reads `Reviews.csv` using Pandas.
   - **EDA**: Generates a bar plot of review counts by star rating.
   - **Sentiment Analysis**: Uses RoBERTa to compute sentiment scores.
   - **Visualization**: Plots positive sentiment scores by star rating using Seaborn.

3. **Outputs**:
   - Bar plot: Review counts per star rating.
   - Bar plot: Average positive sentiment score (`roberta_pos`) by star rating.

## Project Structure

```
sentiment-analysis-amazon-reviews/
├── Sentiment_Analysis_Notebook.ipynb  # Main Jupyter Notebook
├── Reviews.csv                       # Dataset (download from Kaggle)
├── requirements.txt                  # Dependencies
├── README.md                         # This file
```

## Results

- Most reviews are 5-star, as shown in the review count bar plot.
- Positive sentiment scores from RoBERTa increase with higher star ratings, visualized in the "Positive score by star review" plot.

## Future Improvements

- Enhance text preprocessing (e.g., stop word removal, lemmatization).
- Compare RoBERTa with other models like VADER or BERT.
- Analyze negative and neutral sentiment scores.
- Optimize for large-scale data processing.

## Acknowledgments

- [Kaggle](https://www.kaggle.com) for the dataset.
- [Hugging Face](https://huggingface.co) for the RoBERTa model.
- Open-source contributors for Pandas, NLTK, Matplotlib, Seaborn, and Transformers.
