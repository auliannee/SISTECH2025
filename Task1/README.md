# Coursera Web Scraping

## Data Source:
https://www.coursera.org/courses?page=

## Feature Collected
- Course titles
- Organizations offering the courses
- Skills taught in each course
- Course ratings
- Review counts
- Difficulty levels (metadata)

588 courses scraped from 84 pages worth of course listings

## Tools Used
- BeautifulSoup: Our HTML parsing hero
- Requests: For fetching web pages
- Pandas: Data organization wizard

## What I Did
- Extracting text content from course cards
- Handling missing data
- Data Extraction
- Data Preprocessing including Text Normalization, Tokenization using NLTK, Remove Stopwords, and Stemming with Porter Stemmer (so "management" and "managing" become the same thing)

## Reflection
I found it quiet confusing at first but found out that Coursera's web is pretty scraper-friendly with consistent CSS classes. There are some missing values (None) but it's all good :D

