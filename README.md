# Project Name: Exploring ESG Sentiment and Financial Performance

## Project Goals and Summary

### Research Question and Relevance

This project demonstrates the use of data scraping and natural language processing methods in Python to perform a sentiment analysis on annual report (10-K) SEC filings of randomly selected companies from all sectors, specifically focusing on the sentiment around the corporate ESG disclosure.

The primary research questions explored in the project are:

1. How does overall sentiment within ESG disclosures correlate with financial performance?
2. Does sentiment within each ESG component (Environmental, Social, Governance) correlate with financial performance?
3. Does investor confidence mediate the relationship between ESG sentiment and financial performance?

These questions are significant because they delve into whether ESG disclosures serve as genuine indicators of corporate health or are used by companies to mask underlying issues. By exploring the impact of ESG sentiments on financial performance and investor confidence, this research contributes to understanding the real value of ESG disclosures in the financial domain and provides insights for understanding corporate influence, analyzing investor behavior and informing policy and regulation, which contributes to the development of effective regulatory frameworks, promoting responsible corporate practices and market integrity.

### Project Summary and Main Findings

The project aimed to explore the relationship between ESG sentiment and financial performance, focusing on whether positive ESG disclosures reflect genuine corporate health or serve as a facade. Through data collection from the Orbis database and EDGAR filings, sentiment analysis using a supervised training model, and regression analysis, the study found that:

- ESG sentiment scores range from -1 to +1, with a mean positive sentiment, indicating a general trend of companies reporting positively on ESG matters.
- Regression analysis showed a statistically significant positive relationship between total ESG score and return on equity, suggesting companies are not inclined to conceal poor financial performance through positive ESG disclosures.
- The research highlights the role of investor confidence as a mediating factor in the relationship between ESG sentiment and financial performance, offering insights into corporate, investor, and regulatory dynamics in the context of ESG reporting.

- The regression of total ESG score on ROE shows a positive relationship, and the positive coefficient is statically significant at 1%. Profitability performance is positively correlated with the degree of positivity of ESG tone. Thus we can conclude that the companies are generally not inclined to conceal the bad financial performance using positive ESG content. If the overall financial performance is good, companies tend to report financial performance in a more positive tone. In other words, the firms in our sample are choosing to disclose “honestly” to the public.

- In the regression of separate Environment, Social and Governance score, overall, we obtain similar results. If the overall financial performance is good, companies tend to report environmental and social responsibility performance in a more positive tone. We don’t find significant correlation in the separate regression of Governance score in terms of financial performance. we can conclude that the companies in our sample are generally not inclined to conceal the bad financial performance using positive ESG content. 

## How to Navigate This Repository

### Repository Structure
This repository is structured to support a comprehensive project focusing on dynamic web scraping, data cleaning and preprocessing, ESG sentiment analysis, and visualization of regression results, primarily within the context of financial and ESG data. 

Below is a brief description of each directory and its contents:

Code: This directory contains Jupyter Notebooks and scripts pivotal to the project's execution:
- Dynamic Scraping: A Jupyter Notebook equipped with Selenium for browser automation, BeautifulSoup for parsing HTML, and Pandas for data manipulation. It automates the extraction of specific information from dynamic web pages.

- ESG Sentimental Analysis: A Python script for conducting sentiment analysis on ESG-related content, utilizing various libraries for data preprocessing, keyword identification, and sentiment scoring.
- Data Cleaning and Preprocessing Notebook: Focuses on cleaning and preprocessing a dataset that merges ESG scores with financial metrics of companies, preparing it for analysis.
- Visualization: Contains scripts or notebooks designed to visualize regression results, enhancing the interpretability of the analysis.

Data: This directory hosts essential data files for the project:
- Full_data.xlsx: Contains the 10-K filings and additional information like CIK and adjusted names of companies.
- LM Sentiment Dictionary: Includes lists of positive and negative words used in sentiment analysis.
- Link_to_bin.md: Provides a Google Drive link to the `GoogleNews-vectors-negative300.bin.gz` file, which is too large for direct GitHub upload.
- data_2022_cleaned.csv: ESG sentiment data of last year, used for the last regression about investor sentiment.

Slides: Comprises presentation materials used to summarize and present the project findings:
- ESG_Final: The initial version of the slide deck presented in class.
- ESG_Final_updated: The revised and final version of the slide deck post-presentation, incorporating feedback and additional insights.


### Running the Code
- Data scraping: run the “scrapping.ipynb”, be sure that the “company_info.xlsx” is under the same path of this notebook (you will need to load it when matching two datasets) 
- Sentiment Analysis: run “Sentiment_analysis.ipynb”
- Data cleaning: run the “Cleaning.ipynb”
- Data Analysis & Visualization: run “Analysis.ipynb”


## Data Sources

- 1.Direct filtered and download financial performance indicator data (ROE, Total Asset, Solvency ratio) from Orbis database: https://login.bvdinfo.com/R1/Orbis
- 2.Scrapped ESG content used for sentiment analysis from financial report：EDGAR filing - 10K annual financial report: https://www.sec.gov/edgar/searchedgar/companysearch
- 3.Pre-trained word embeddings for NLP tasks: `GoogleNews-vectors-negative300.bin.gz` - 300-dimensional Word2Vec model trained on Google News dataset, suitable for a variety of language processing applications. https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit?resourcekey=0-wjGZdNAUop6WykTtMip30g

## Dependencies

### Name                  Version               
- selenium                  4.9.0    
- requests                  2.28.1
- beautifulsoup4            4.11.1
- pandas                    1.4.4
- numpy                     1.24.3
- regex                     2022.7.9
- en-core-web-sm            3.7.1             
- nltk                      3.8.1  
- spacy                     3.7.4 
- docstring-to-markdown     0.11 
- scikit-learn              1.3.0
- matplotlib                3.7.1
- statsmodels               0.14.0
- seaborn                   0.12.2
- wordcloud                 1.9.3


## Team Contributions

- **In-class Presentation & Slides**: Jiale Zhou and Yu Hui were responsible for the in-class presentation, including the creation of engaging slides and updating new slides.

- **Short Video**: Zhicheng You and Yuanhan Cui took charge of producing a concise video that encapsulates the essence and key findings of our project. This task required scripting, filming, and editing, aiming to provide an informative yet engaging summary suitable for a broad audience.

- **README Documentation**: All group members collectively contributed to the README documentation. This document serves as a detailed guide to our project, outlining the objectives, methodology, findings, and conclusions, ensuring that our research is transparent and replicable.

- **Data Collection (Web Scraping & Extracting ESG-Related Text)**: Yu Hui and Zhicheng You led the data collection process, utilizing web scraping techniques to gather relevant text data on ESG factors. This foundational work was crucial for our analysis and the overall success of the project.

- **Sentiment Analysis**: Yuanhan Cui and Jiale Zhou focused on the sentiment analysis component, employing NLP  tools  to assess the emotional tone of the ESG-related texts and using semantic similarity methods to construct ESG dictionaries.

- **Regression Analysis and Visualization**: Yu Hui and Zhicheng You specialized in regression analysis and data visualization, creating informative and aesthetically pleasing visuals to represent our findings effectively. These visualizations play a key role in making our research accessible and understandable to a wider audience.


## Presentation Slides and Video

### In-Class Presentation Slides
(Add a link to the in-class presentation slides uploaded to the repository. Specify the file name or provide a direct link to view or download the slides.)

### Updated In-Class Presentation Slides
(If the presentation slides were updated after the class presentation, provide a link to the updated version uploaded to the repository.)

### Video
Part1 Introduction & Data Scraping:
https://drive.google.com/file/d/1kkInBAISvWX7kfT83O1zVbuKK4cRF0xu/view?usp=share_link

Part 2: Sentiment Analysis
https://drive.google.com/file/d/14VQzbeE-OdH_bEzTXmG41oTqfrPdJMVx/view?usp=share_link

Part3&4 Data Cleaning & Analysis: https://drive.google.com/file/d/1rJZo4vUyi9NRIm93svfGyyGjOlyV0rsV/view?usp=share_link

---

(You may also want to include sections for License, Acknowledgments, and How to Contribute, depending on the nature and scope of your project.)
