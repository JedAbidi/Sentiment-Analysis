Sentiment Analysis on Amazon Fine Food Reviews
Project Overview
This project performs sentiment analysis on the Amazon Fine Food Reviews dataset using Python. The goal is to analyze customer reviews to determine their sentiment (positive, negative, or neutral) based on review text and star ratings. The project leverages libraries like NLTK, Pandas, Matplotlib, Seaborn, and a pre-trained RoBERTa model for sentiment analysis.
Dataset
The dataset used is the Amazon Fine Food Reviews dataset available on Kaggle. It contains over 568,000 reviews of food products sold on Amazon, with features including:

Columns: Id, ProductId, UserId, ProfileName, HelpfulnessNumerator, HelpfulnessDenominator, Score, Time, Summary, Text
Key Features:
Score: Star rating (1 to 5) given by the reviewer.
Text: The review text provided by the customer.


Size: 568,454 rows and 10 columns.

The dataset is used to visualize review distributions and perform sentiment analysis using the RoBERTa model to compute sentiment scores.
Installation
To run this project, ensure you have Python 3.10 installed along with the required libraries. Follow these steps to set up the environment:

Clone the Repository:
git clone https://github.com/your-username/sentiment-analysis-amazon-reviews.git
cd sentiment-analysis-amazon-reviews


Install Dependencies:Create a virtual environment and install the required packages:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt


Requirements:The requirements.txt file includes:
nltk
pandas
numpy
matplotlib
seaborn
transformers


Download the Dataset:

Download the dataset from Kaggle.
Place the Reviews.csv file in the project directory or update the file path in the notebook.


Optional GPU Setup:The project supports GPU acceleration (e.g., NVIDIA Tesla T4). Ensure CUDA and cuDNN are installed if running on a GPU-enabled system.


Usage

Run the Jupyter Notebook:Start Jupyter Notebook and open the Sentiment_Analysis_Notebook.ipynb file:
jupyter notebook Sentiment_Analysis_Notebook.ipynb


Key Steps in the Notebook:

Data Loading: Loads the Amazon Fine Food Reviews dataset using Pandas.
Exploratory Data Analysis (EDA):
Displays the first few rows of the dataset.
Visualizes the distribution of star ratings using a bar plot.


Sentiment Analysis:
Uses the RoBERTa model to compute sentiment scores (roberta_pos, etc.) for review texts.
Visualizes positive sentiment scores by star rating using Seaborn.


Output: Generates visualizations like bar plots to interpret sentiment trends.


Expected Outputs:

Bar plot showing the count of reviews by star rating.
Bar plot showing the average positive sentiment score (from RoBERTa) for each star rating.



Project Structure
sentiment-analysis-amazon-reviews/
├── Sentiment_Analysis_Notebook.ipynb  # Main Jupyter Notebook
├── Reviews.csv                       # Dataset (not included in repo, download from Kaggle)
├── requirements.txt                  # Python dependencies
├── README.md                         # This file

Results

The dataset contains a significant number of reviews, with a majority rated 5 stars, as visualized in the review count bar plot.
The RoBERTa model provides sentiment scores, and the positive sentiment score (roberta_pos) correlates with higher star ratings, as shown in the bar plot titled "Positive score by star review."

Future Improvements

Add preprocessing steps for text cleaning (e.g., removing stop words, lemmatization).
Incorporate additional sentiment models for comparison (e.g., VADER, BERT).
Expand analysis to include negative and neutral sentiment scores.
Optimize for large-scale processing by sampling or using distributed computing.





Acknowledgments

Kaggle for providing the Amazon Fine Food Reviews dataset.
Hugging Face for the RoBERTa model used for sentiment analysis.
The open-source community for the libraries used in this project.
