# Twitter-Sentiment-Analysis using BERT
This project performs sentiment analysis on Twitter data using a fine-tuned BERT model.
It get real-time Twitter search data then classifies it into three categories: Positive, Negative, or Neutral, then saves the results to a CSV file and visualizes the sentiment distribution.

## Overview
The system connects to the Twitter API to collect live tweets, processes them using a BERT-based model, and classifies their sentiment. 

-The final output includes:

Predicted sentiment labels

Exported results to a CSV file

A sentiment distribution chart

## Features

-Collects live data from Twitter

-Preprocesses and tokenizes text

-Classifies sentiment using BERT

-Supports 3 sentiment classes (Positive, Negative, Neutral)

-Saves predictions in CSV format

-Generates a visual sentiment summary (bar chart or pie chart)

## Dataset

-Sources:Datasets from Kaggle

-Preprocessing:

Cleaned text (punctuation, Hashtags, mentions)

Removed short/irrelevant text

Balanced to include 33,000 rows for each class of three classes

## Model

-Architecture: bert-base-uncased 

-Training:

    Fine-tuned on the cleaned dataset

    Trained using GPU in Google Colab

-Optimizer: AdamW

-Loss: CrossEntropyLoss

-Output:

    Sentiment label (0 = Negative, 1 = Neutral, 2 = Positive)

-Results

    Accuracy: ~85%

-Evaluated using:

    Confusion Matrix

    Classification Report (Precision, Recall, F1-Score)

    Strong performance across all three classes

## Future Work

    -Deploy as a web app 

    -Add multilingual sentiment support

    -Integrate a feedback loop to improve predictions over time

    -Extend to other platforms (e.g., Facebook, google, YouTube comments)

