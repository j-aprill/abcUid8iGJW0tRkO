# 🎯 AI-Powered HR Candidate Ranking & Semantic Matching Pipeline (`Final_Model.ipynb`)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![NLP](https://img.shields.io/badge/NLP-Semantic%20Similarity%20%7C%20Embeddings-purple.svg)]()
[![Domain](https://img.shields.io/badge/Domain-HR%20Tech%20%26%20Talent%20Sourcing-teal.svg)]()
[![Status](https://img.shields.io/badge/Status-Complete-success.svg)]()

> An end-to-end Natural Language Processing (NLP) pipeline designed to automate and optimize Human Resources talent sourcing by ranking LinkedIn candidate profiles based on their semantic similarity to target role phrases and hiring criteria. This pipeline impliments a "human in the loop" (hitl) feedback mechanism where candidates can be reranked based on "starring" the candidates. Candidates who have similiar headlines to starred candidates will be ranked higher. 

---

## 🎯 Executive Summary 
* **Core Problem Solved:** Automated the manual, time-consuming screening of candidate LinkedIn profiles by building an objective, NLP-based similarity ranking engine.
* **Technical Competency:** Applied text preprocessing, vectorization/embedding techniques (TF-IDF), and cosine similarity scoring in Python.
* **Business Impact:** Enables HR and talent acquisition teams to instantly surface top-matching candidates for specific job requirements while maintaining transparency into *why* candidates ranked highly. It also empowers HR to star certain candidates and then have the pipeline rerank candidates based on the starring action.

---

## 🔄 Project Workflow & Step-by-Step Flow

Here is the structured NLP and information retrieval pipeline built within the Final Model:

### Step 1: Data cleaning
* **Duplicate Removal:** Removed duplicates from the data set to ensure they do not affect the weight of certain words or candidates.
* **Text Normalization:** Cleaned raw profile text by removing special characters, extra spaces, and standaardizing the terminology (e.g HR versus Human Resources).

### Step 2: 1st Ranking Vectorization & Semantic Representation
* **Feature Extraction:** Transformed candidate headlines into dense numerical vector representations using TF-IDF vectorization and scaled numerical connections data.
* **Formula Creation:** created a formula that would combine the keywords vectorization in the headline and the number of connections on linked into to create an initial fit score between 0 and 1.

### Step 3: Reranking
* **Cosine Similarity Calculation:** Computed pairwise similarity scores between each candidate's profile vector and starred candidates headlines.
* **Ranking & Reranking Engine:** Aggregated similarity scores across target phrases to generate a ranked leaderboard of top candidates, including optional re-ranking adjustments based on a starring action.

### Step 4: Automating it
* **Creating a Function:** Once the initial rank and rerank were working, these were combined into a single function that could be customized and used for other projects. The function accepts a data frame, indices of starred candidates, and custom target phrases. 

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **NLP & Text Processing:** Scikit-Learn, cosine_similarity, TfidfVectorizer
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib 
* **Environment:** Jupyter Notebook

---

## 💡 Key Technical Highlights & Design Decisions

* **Semantic Matching vs. Rigid Keyword Filters:** Traditional Applicant Tracking Systems (ATS) miss qualified talent due to rigid keyword rules. By ranking profiles via vector similarity, and allowing hirers to go back an star certain candidates, this pipeline captures contextual relevance even when candidates use slightly different terminology.
* **Explainable Ranking Scores:** Outputted clear similarity scores alongside the profile attributes so hiring teams can audit and trust the candidate rankings.

---

## 🏁 Concluding Remarks & Future Scope

### What This Project Demonstrates
This project highlights my ability to apply Natural Language Processing to a real-world HR business problem: turning unstructured profile text into an automated, ranked talent pipeline.


