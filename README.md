# News Popularity EDA Project

This project explores and analyzes a dataset of news articles and their popularity across multiple social media platforms. The workflow includes data loading, cleaning, exploratory data analysis (EDA), text preprocessing, and preparation for predictive modeling.

---

## Project Structure

```
.
├── train_file.csv                 # Training dataset
├── test_file.csv                  # Test dataset
└── news-popularity-eda-1.ipynb    # Main Jupyter Notebook for EDA
```

---

## Dataset Description

**Key Features:**

- **IDLink**: Unique article identifier  
- **Title**: News article title  
- **Headline**: News article headline  
- **Source**: Publisher of the news item  
- **Topic**: Main topic/category of the article (e.g., economy, obama)  
- **PublishDate**: Date and time of publication  
- **GooglePlus**: Popularity score on Google+  
- **SentimentTitle**: Sentiment score of the title  
- **SentimentHeadline**: Sentiment score of the headline  
- **cleaned_title/headline**: Lowercased, punctuation-removed versions  
- **lemmatized_title/headline**: Lemmatized text for analysis  

The dataset is designed to analyze which factors influence the popularity of news articles on social media platforms[1][5].

---

## How to Run

1. **Install Requirements**

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

2. **Open the Notebook**

   - Launch `news-popularity-eda-1.ipynb` in Jupyter Notebook or Google Colab.

3. **Execute All Cells**

   - Run each cell in order to perform data loading, cleaning, EDA, and text preprocessing.

---

## Workflow Overview

### 1. Data Loading

- Reads `train_file.csv` and `test_file.csv` for analysis[1].

### 2. Data Inspection

- Displays the first few rows and checks column types and missing values.
- Key columns include article ID, title, headline, source, topic, publish date, popularity metrics, and sentiment scores.

### 3. Data Cleaning

- Handles missing values and standardizes text (lowercasing, removing punctuation).
- Creates cleaned and lemmatized versions of titles and headlines for NLP tasks.

### 4. Exploratory Data Analysis (EDA)

- **Distribution Analysis**: Examines distributions of article topics, sources, and publish dates.
- **Popularity Metrics**: Analyzes popularity scores across platforms (Google+, Facebook, LinkedIn if available).
- **Sentiment Analysis**: Explores the sentiment of titles and headlines and their relationship to popularity.
- **Text Analysis**: Looks at headline/title lengths, word counts, and most common words[3][5].

### 5. Text Preprocessing

- Cleaning and lemmatizing text for further natural language processing.
- Prepares data for feature engineering and modeling.

---

## Example: Code Snippet for Data Loading and Inspection

```python
import pandas as pd

# Load dataset
df = pd.read_csv('train_file.csv')

# Display first 5 rows
print(df.head())

# Check for missing values
print(df.isnull().sum())
```

---

## Recommendations & Notes

- **Data Quality**: The notebook handles missing values and text normalization, which is essential for NLP tasks.
- **EDA**: Visualizations (histograms, bar charts) are used to understand distributions and relationships.
- **Text Features**: Cleaned and lemmatized columns are created for advanced text analysis.
- **Modeling**: While this notebook focuses on EDA, the cleaned and processed data is suitable for regression or classification models to predict popularity scores[4][5].

---

## Summary

This project provides a comprehensive exploratory analysis of news article popularity across social media. It includes robust data cleaning, insightful EDA, and thorough text preprocessing, setting a strong foundation for predictive modeling or further NLP tasks.

---

