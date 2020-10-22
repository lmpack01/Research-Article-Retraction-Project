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
The goal of this project is to collect and process data related to retracted and non-retracted published academic literature. Non-retracted article data will be taken from the PLOS ONE journal, while retracted article data will be taken across all readily accessible journals in the PubMed database. This data will be used to determine if there are any key trends between the metadata of each article and if that article was later retracted. Additionally, this data will be used to create a NLP model that will be able to determine if a paper will be retracted based on its corpus. Several metrics will be used to assess the performance of the model, including accuracy and sensitivity. 

This project is important to researchers, as researchers would be able to determine if a paper they create needs to be edited to avoid common reasons for retraction, such as plagiarism. Additionally, editors of journals could use the model created in this project to quickly determine if a newly submitted article needs to be looked over closely before moving the article forward in the publishing process. 

For the general public, this project will highlight any prevalent trends in topics or scientific methods that are more likely to be retracted. By having a healthy conversation about the dynamics of retraction, we can build a greater trust between the general public and the scientific community. 

---

### Data Collection


---

### Data Cleaning


---

### Feature Engineering


---

### EDA


---

### Naive Bayes Models
 

---

### Decision Tree Models


---

### CSV Files


---

### Useful Resources
* [Biopython documentation](https://biopython.org/)
* [Entrez Programming Utilities documentation](https://www.ncbi.nlm.nih.gov/books/NBK25497/)
* [PMC Database](https://www.ncbi.nlm.nih.gov/pmc/)
* [PubMed Database](https://pubmed.ncbi.nlm.nih.gov/)

---

### Data Acquisition


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
