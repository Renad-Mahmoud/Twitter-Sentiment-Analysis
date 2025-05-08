# RealTime_Twitter-Sentiment-Analysis using BERT
## Overview
This project is designed to provide an end-to-end solution for understanding the sentiment of social media posts(Twitter). 

The project prepares a balanced dataset, fine-tunes a high-performing BERT model for sentiment classification, and implements a real-time pipeline to analyze and visualize live tweets. It achieves 85% accuracy with strong evaluation metrics, making it effective for real-world sentiment analysis.

# Notebooks Description

## Data Preparation (Data_Preparation.ipynb)
    - This notebook handles the preprocessing and preparation of the sentiment dataset:

    - Merges 4 different Kaggle datasets into a unified format.

    - Cleans the data by removing null values, duplicates, and very short texts.

    - Balances the dataset by selecting 33,000 samples for each sentiment class.

    - Shuffles and resets the index to prepare the data for training.

    - Output: A clean and balanced dataset ready for model training. 

## BERT Model Training (bert_Sentiment_analysis.ipynb)
    - This notebook fine-tunes a BERT-based transformer model for sentiment classification:

    - Loads and tokenizes the cleaned dataset.

    - Splits data into train, test and validation sets with stratify to preserve class distribution.

    - Fine-tunes the model using GPU acceleration.

    - Evaluates the model using accuracy, confusion matrix, precision, recall, and F1-score.

    - Saves the trained model for future inference.

    - Final Accuracy: 85%

## Real-Time Twitter Sentiment Pipeline (real_time_Twitter_Sentiment_analysis.ipynb)
    - This notebook creates a real-time pipeline to collect and analyze tweets:

    - Uses the Twitter API to collect tweets based on specific keywords or hashtags.

    - Preprocesses and feeds the live tweets into the fine-tuned BERT model.

    - Predicts sentiment labels (Positive, Negative, Neutral) for each tweet.

    - Saves results (tweet text, sentiment, metadata) into a .csv file.

    - Visualizes the sentiment distribution using graphs for better interpretation (bar, pie chart).

    - Output: A CSV + visual sentiment summary.

### Finally, you simply enter a topic or keyword, and the system will fetch relevant live tweets, analyze their sentiment save the results to a CSV file, and generate visualizations for better sentiment insight.

## Future Work

    - Deploy as a web app 

    - Add multilingual sentiment support

    - Integrate a feedback loop to improve predictions over time

    - Extend to other platforms (e.g., Facebook, google, YouTube comments)

