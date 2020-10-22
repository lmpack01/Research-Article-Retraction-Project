# Research Article Retraction Project

![alt text](https://github.com/lmpack01/Research-Article-Retraction-Project/blob/main/images/martin-adams-_OZCl4XcpRw-unsplash.jpg?raw=true)
<span>Photo by <a href="https://unsplash.com/@martinadams?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Martin Adams</a> on <a href="https://unsplash.com/s/photos/research?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>

---

### Table of Contents
* [Author](#author)
* [Problem Statement](#problem-statement)
* [Data Collection](#data-collection)
* [Data Cleaning](#data-cleaning)
* [Feature Engineering](#feature-engineering)
* [EDA](#eda)
* [Naive Bayes Models](#naive-bayes-models)
* [Decision Tree Models](#decision-tree-models)
* [CSV Files](#csv-files)
* [Useful Resources](#useful-resources)
* [Data Acquisition](#data-acquisition)
* [Requirements](#requirements)

---

### Author
This repository was created by Larissa Pack. 

---

### Problem Statement
The goal of this project is to collect and process data related to retracted and non-retracted published academic literature. Non-retracted article data will be taken from the PLOS ONE journal, while retracted article data will be taken across all readily accessible journals in the PubMed database. This data will be used to determine if there are any key trends between the metadata of each article and if that article was later retracted. Additionally, this data will be used to create a NLP model that will be able to determine if a paper will be retracted based on its corpus. Several metrics will be used to assess the performance of the model, including accuracy, sensitivity, precision, and the number of correct retractions detected (true positives). 

This project is important to researchers, as researchers would be able to determine if a paper they create needs to be edited to avoid common reasons for retraction, such as plagiarism. Additionally, editors of journals could use the model created in this project to quickly determine if a newly submitted article needs to be looked over closely before moving the article forward in the publishing process. 

For the general public, this project will highlight any prevalent trends in topics or scientific methods that are more likely to be retracted. By having a healthy conversation about the dynamics of retraction, we can build a greater trust between the general public and the scientific community. 

---

### Data Collection
Data collection was ultimately a four step process for accessing both retracted and non-retracted articles:

1. Determine the journal name for the articles
2. Use this journal name as a search term for querying the PubMed database with the biopython library
3. Use the PubMed query to determine the DOI for each article
4. Use the DOI of each article to query the PMC database with the biopython library for the full-text of the article

This process was repeated for over 10,000 articles. Information pulled from these queries was saved in CSV files.

---

### Data Cleaning
The retraction and no retraction data were cleaned. CSV files were joined appropriately, null values were dropped where necessary, keywords were unpacked from strings, and the full-text of each article was cleaned using different methods. Once both dataframes were cleaned, they were joined together and evaluated for duplicates. Information was saved into CSV files throughout the cleaning process.

---

### Feature Engineering
Several feature engineered columns were created within the cleaned dataframes. A keyword binary column was created to represent if the article used keyword lists. General NLP columns related to word count and character length were created. Several columns were created based on typical concepts found in academic literature that may show trends in topics for retracted articles, such as columns discussing the presence of animal studies, human studies, if the article was a review paper, and if the article discussed novel ideas. Text readability columns were created as well. These columns were saved into CSV files.

---

### EDA
Metadata about the articles determined during the querying process was visualized as well as the feature engineering that took place in the previous notebook. A correlation coefficient heatmap showed that the only metadata that had a correlation to the article being retracted was the presence of a keyword list. General trends that were noticed in the other visualizations were discussed.

---

### Naive Bayes Models
A baseline model was created and the implications of that model were discussed. A stopwords list was created that better served common stopwords in academic literature. A function was created to run multinomial Naive Bayes models with differing parameters. For each model ran, the training accuracy, testing accuracy, sensitivity, precision, and the number of correct retractions detected was determined. The models were compared to each other and the appropriate vectorizer parameters were determined for subsequent modeling.

---

### Decision Tree Models
A function was created to run different variants of decision tree classifier models with differing parameters. The parameters for the model best optimized for sensitivity and the number of correct retractions detected was determined after significant testing. The most common bigrams using the appropriate vectorizer parameters were determined for retracted articles and non-retracted articles only. The most common words using the appropriate vectorizer parameters were determined for retracted articles and non-retracted articles only. The implications of both the bigrams and the single words were discussed. The feature importance values for the optimized model were explored. 

---

### CSV Files
The cleaned CSV file that contains the journals that participate fully in the PMC database is included in the "datasets" folder. Due to the size and number of CSV files that were created during this project, the other CSV files will not be published on GitHub. Please feel free to contact me if you would like access to a specific CSV file.

---

### Useful Resources
* [Biopython documentation](https://biopython.org/)
* [Entrez Programming Utilities documentation](https://www.ncbi.nlm.nih.gov/books/NBK25497/)
* [PMC Database](https://www.ncbi.nlm.nih.gov/pmc/)
* [PubMed Database](https://pubmed.ncbi.nlm.nih.gov/)

---

### Data Acquisition
This data was acquired using the biopython library in conjunction with the PubMed and PMC databases. Thank you to the National Library of Medicine at the U.S. National Institutes of Health for giving free access to such a large archive of incredible knowledge. Thank you to the team of developers who created and upkeep the biopython library for giving others the ability to easily work with this archive. Without these groups, this project would not have been possible. 

---

### Requirements
Anaconda3 with Python, Jupyter Notebooks, and Python libraries including: 
* biopython 
* pandas 
* requests 
* time 
* bs4 
* numpy 
* matplotlib.pyplot 
* seaborn 
* nltk, specifically: 
    * .corpus 
    * .stem 
    * .tokenize 
* sklearn, specifically: 
    * .ensemble 
    * .model_selection 
    * .feature_extraction.text 
    * .naive_bayes 
    * .metrics 
    * .tree 
* textstat
