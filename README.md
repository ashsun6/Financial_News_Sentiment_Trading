# Financial News Sentiment Analysis for Trading

A scalable machine learning pipeline that analyzes financial news sentiment to make trading decisions using Apache Spark and big data tools.

## Project Overview

This project builds a sentiment-driven trading system that processes millions of financial news articles to predict market movements. The system demonstrates the application of big data technologies to financial analysis, processing ~26GB of news data and historical price information.

## Key Features

- **Scalable Data Processing**: Handles 15+ million financial news articles using Apache Spark
- **Custom ML Pipeline**: Built from scratch using Spark MLlib with TF-IDF vectorization and logistic regression
- **Financial-Focused Sentiment Analysis**: Uses domain-specific word lists (Loughran-McDonald Financial Dictionary)
- **Backtesting Framework**: Evaluates trading strategies against historical price data
- **Big Data Infrastructure**: Leverages Hadoop HDFS, Google Cloud Dataproc, and distributed computing

## Procedure

The pipeline consists of several stages:

1. **Data Ingestion**: Raw financial news and price data stored in HDFS
2. **Data Preprocessing**: Multi-line CSV parsing and conversion to optimized Parquet format
3. **Feature Engineering**: TF-IDF vectorization of article content
4. **Sentiment Labeling**: Custom scoring based on financial sentiment word lists
5. **Model Training**: Multinomial logistic regression for sentiment classification
6. **Strategy Evaluation**: Backtesting against historical price movements

## Data Sources

- **Financial News**: ~26GB Nasdaq financial articles dataset (15M+ articles)
- **Historical Prices**: 4,700+ CSV files with daily stock prices
- **Sentiment Lexicons**: 
  - Loughran-McDonald Financial Sentiment Dictionary
  - Liu Bing Opinion Word List

## Tools

- **Apache Spark**: Distributed data processing and machine learning
- **PySpark**: Python API for Spark
- **Hadoop HDFS**: Distributed file system for data storage
- **NYU Google Cloud Dataproc**: Managed Spark clusters
- **Jupyter Notebook**: Interactive development environment
- **Parquet**: Columnar storage format for optimized queries

## Results

The model was trained on 2M+ articles and tested on 500K+ articles:

- **Training Performance**: 51% accuracy on long positions, 49.8% on short positions
- **Test Performance**: 50.9% accuracy on long positions, 49.6% on short positions
- **Strategy Returns**: Near-zero average returns with high volatility, indicating limited predictive power

## Key Insights

- Sentiment analysis alone provides minimal edge in trading decisions
- The system successfully demonstrates scalable processing of financial big data
- Model shows no overfitting with consistent train/test performance
- Financial news sentiment may require more sophisticated feature engineering for profitable trading

## Files

- `financial_news_sentiment_analysis.ipynb`: Main Jupyter notebook with complete pipeline
- `financial_news_sentiment_analysis.pdf`: PDF version of the notebook