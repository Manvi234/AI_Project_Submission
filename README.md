# AI Project Submission – Employee Sentiment Analysis

## Overview

This project analyzes employee emails to evaluate overall sentiment, rank employees, identify flight risks, and model sentiment trends using Natural Language Processing (NLP) and linear regression. The dataset consists of unlabeled email messages, which are processed and labeled using sentiment analysis techniques.

## Project Structure

| Step | Task |
|------|------|
| 1   | Data Cleaning & Preprocessing |
| 2   | Sentiment Labeling with TextBlob |
| 3   | Exploratory Data Analysis (EDA) |
| 4   | Monthly Sentiment Scoring (Employee-wise) |
| 5   | Employee Ranking (Top 3 Positive & Negative per Month) |
| 6   | Flight Risk Identification (Rolling 30-day Rule) |
| 7   | Linear Regression Model for Trend Prediction |

## Key Components & Results

### Sentiment Labeling

Each email is labeled as:
- Positive if polarity > 0.1
- Negative if polarity < -0.1
- Neutral otherwise

A sentiment score is stored for trend and modeling.

### EDA Highlights

- Distribution of sentiment labels
- Email body length histogram
- Top 10 email senders
- Monthly sentiment score trend

### Monthly Sentiment Scoring

Each employee receives a monthly sentiment score:
- +1 for Positive
- -1 for Negative
- 0 for Neutral

Used to assess individual performance and engagement.

### Employee Ranking

- Top 3 Positive Employees per month: Highest monthly sentiment scores
- Top 3 Negative Employees per month: Lowest (most negative) scores

Sorted by score and then alphabetically for consistency.

### Flight Risk Identification

Employees are flagged as flight risks if:
They send 4 or more Negative emails in any 30-day rolling window.

List of flagged employees includes:
- bobette.riner@ipgdirect.com
- sally.beck@enron.com
- john.arnold@enron.com
- and others

### Linear Regression Trend Model

Objective: Predict sentiment trend over time.

Features:
- message_count, message_length, word_count, and subject_length
- Target: Monthly average sentiment score

The model captures sentiment drift and organizational mood trends with a clear trendline plot.

## Summary

Top 3 Positive Employees for January 2010:
- kayne.coulter@enron.com (Score: 5)
- patti.thompson@enron.com (Score: 5)
- don.baughman@enron.com (Score: 4)

Top 3 Negative Employees for January 2010:
- rhonda.denton@enron.com (Score: 0)
- johnny.palmer@enron.com (Score: 1)
- bobette.riner@ipgdirect.com (Score: 2)

Flight Risk Employees:
- Identified using rolling 30-day negative email rule

## Tools Used

- Python (Pandas, Matplotlib, Seaborn, Scikit-learn)
- TextBlob for Sentiment Analysis
- Jupyter Notebook

## Instructions

- Run the notebook cell by cell
- Ensure all packages (`textblob`, `sklearn`, etc.) are installed
- Final plots and outputs will appear inline

## Author

Your Full Name  
Email: your.email@example.com  
Project: AI-project-submission
