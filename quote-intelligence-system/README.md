# Quote Intelligence System

An end-to-end web scraping and data preprocessing project built using Python.  
This project focuses on **data acquisition, cleaning, and structuring**, forming a reusable dataset for downstream analytics and machine learning tasks.

---

## Project Overview

In real-world AIML workflows, data is not always readily available in clean datasets.  
This project demonstrates how to **collect raw textual data from the web**, process it, and transform it into a structured format suitable for analysis or machine learning models.

The system scrapes multi-page quote data from a public website, extracts relevant information such as quote text, author, and tags, and stores the cleaned data in CSV format.

---

## Key Features

- Multi-page web scraping using dynamic pagination
- Raw HTML storage for reproducibility and offline parsing
- HTML parsing using BeautifulSoup with CSS selectors
- Structured data extraction (quote, author, tags)
- Data cleaning and filtering using Pandas
- Export of processed dataset in CSV format for ML usage

---

## Tech Stack

- **Python**
- **Requests** – HTTP requests and page retrieval
- **BeautifulSoup (bs4)** – HTML parsing and DOM traversal
- **lxml** – Fast HTML parser
- **Pandas** – Data cleaning, filtering, and CSV handling

---

## Folder Structure

```text
quote_intelligence_system/
│
├── notebooks/
│ └── web_scraping.ipynb
│
├── data/
│ ├── raw/
│ │ └── quotes_page_1.html
│ │ └── quotes_page_2.html
│ │ └── ...
│ │
│ └── processed/
│ └── life_quotes.csv
│
├── requirements.txt
└── README.md

``` 

## Dataset Description

The final dataset (`life_quotes.csv`) contains the following columns:

- **quote** – Text of the quote
- **author** – Author of the quote
- **tags** – Comma-separated tags associated with the quote

The dataset is designed to be **machine-readable**, making it suitable for NLP, text classification, clustering, or sentiment analysis tasks.

---

## Why CSV Looks Unaligned

CSV files are meant for **machine consumption**, not visual alignment.  
While the file may not appear visually aligned in text editors, it is correctly structured and can be reliably read using tools like Pandas or Excel.

```python
import pandas as pd
df = pd.read_csv("life_quotes.csv")