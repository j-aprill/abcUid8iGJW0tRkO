# 🎯 AI-Powered HR Candidate Ranking & Semantic Matching Pipeline (`Final_Model.ipynb`)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![NLP](https://img.shields.io/badge/NLP-Semantic%20Similarity%20%7C%20Embeddings-purple.svg)]()
[![Domain](https://img.shields.io/badge/Domain-HR%20Tech%20%26%20Talent%20Sourcing-teal.svg)]()
[![Status](https://img.shields.io/badge/Status-Complete-success.svg)]()

> An end-to-end Natural Language Processing (NLP) pipeline designed to automate and optimize Human Resources talent sourcing by ranking LinkedIn candidate profiles based on their semantic similarity to target role phrases and hiring criteria.

---

## 🎯 Executive Summary (For Recruiters & Hiring Managers)
If you only have 30 seconds, here is what this project demonstrates:
* **Core Problem Solved:** Automated the manual, time-consuming screening of candidate LinkedIn profiles by building an objective, NLP-based similarity ranking engine.
* **Technical Competency:** Applied text preprocessing, vectorization/embedding techniques (e.g., TF-IDF, Word2Vec, or Transformer-based embeddings), and cosine similarity scoring in Python.
* **Business Impact:** Enables HR and talent acquisition teams to instantly surface top-matching candidates for specific job requirements while maintaining transparency into *why* candidates ranked highly.

---

## 🔄 Project Workflow & Step-by-Step Flow

Here is the structured NLP and information retrieval pipeline built within `Final_Model.ipynb`:

### Step 1: Data Ingestion & Profile Parsing
* **Data Consolidation:** Ingested structured and unstructured LinkedIn profile data (job titles, summaries, skills, and experience descriptions).
* **Schema Standardization:** Standardized text fields across candidate records to ensure consistent comparison against target HR search phrases.

### Step 2: Text Cleaning & NLP Preprocessing
* **Text Normalization:** Cleaned raw profile text by removing HTML artifacts, special characters, punctuation, and redundant whitespace, followed by lowercasing.
* **Tokenization & Lemmatization:** Removed noise/stopwords and normalized word forms (lemmatization/stemming) so variations in phrasing (e.g., *"recruiting"* vs. *"recruiter"*) align cleanly.

### Step 3: Vectorization & Semantic Representation
* **Feature Extraction:** Transformed both candidate profile text and target HR query phrases into dense numerical vector representations (using techniques such as TF-IDF vectorization or pre-trained dense text embeddings).
* **Phrase Alignment:** Structured target role phrases to capture key competencies, domain expertise, and seniority markers required for the HR role.

### Step 4: Similarity Scoring & Candidate Ranking
* **Cosine Similarity Calculation:** Computed pairwise similarity scores between each candidate's profile vector and the target query phrase vectors.
* **Ranking & Reranking Engine:** Aggregated similarity scores across target phrases to generate a ranked leaderboard of top candidates, including optional re-ranking adjustments based on exact keyword/skill matches or role relevance.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **NLP & Text Processing:** Scikit-Learn, NLTK / spaCy, Sentence-Transformers / Gensim *(adjust based on exact libraries used)*
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook

---

## 💡 Key Technical Highlights & Design Decisions

* **Semantic Matching vs. Rigid Keyword Filters:** Traditional Applicant Tracking Systems (ATS) miss qualified talent due to rigid keyword rules. By ranking profiles via vector similarity, this pipeline captures contextual relevance even when candidates use slightly different terminology.
* **Explainable Ranking Scores:** Outputted clear similarity scores alongside matched profile attributes so hiring teams can audit and trust the candidate rankings.

---


## 🏁 Concluding Remarks & Future Scope

### What This Project Demonstrates
This project highlights my ability to apply Natural Language Processing and information retrieval techniques to a real-world HR business problem—turning unstructured profile text into an automated, ranked talent pipeline.

### Future Improvements
* [ ] Implement a human-in-the-loop (HITL) feedback mechanism where recruiter "star" actions dynamically re-weight and refine the target query embeddings (Learning-to-Rank).
* [ ] Upgrade embeddings using domain-fine-tuned Sentence-BERT (`SBERT`) models for deeper contextual understanding of job histories.
* [ ] Build an interactive Streamlit or FastAPI interface allowing recruiters to input custom target phrases and view ranked candidate profiles in real time.

---
*Feel free to reach out if you'd like to discuss the NLP pipeline, similarity scoring methodology, or ranking architecture in greater detail!*
