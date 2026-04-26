


This project builds an **end-to-end NLP pipeline** to process raw text data and enable **semantic search**.
The system cleans noisy text, transforms it into meaningful representations, and retrieves similar comments using vector similarity.

The pipeline is implemented using:

* NLTK
* spaCy
* scikit-learn
* Gensim

Dataset is sourced from:

* Hugging Face

---



A media company receives thousands of:

* Customer reviews
* Blog comments
* Article feedback

They need a system to:

* Clean noisy text
* Standardize language
* Convert text into vectors
* Automatically find similar comments

---


### 1. Text Cleaning

* Lowercasing
* Removing HTML tags
* Removing punctuation and special characters

### 2. Tokenization

* Splitting text into individual words using SpaCy

### 3. Stopword Removal

* Removing common words (e.g., "the", "is", "and") using NLTK

### 4. Lemmatization

* Converting words to their base form

  * Example: *running → run*

### 5. Vocabulary Creation

* Creating a unique set of all words in the dataset

### 6. Bag of Words (BoW)

* Converts text into frequency-based vectors

### 7. TF-IDF Vectorization

* Assigns importance scores to words based on frequency

### 8. Word Embeddings

* Using Word2Vec (Gensim) to create dense vector representations

### 9. Sentence Embeddings

* Averaging word vectors to represent full sentences

### 10. Similarity Search

* Using cosine similarity to find similar comments

### 11. Visualization

* Word frequency distribution
* Similarity heatmaps

---



We use the IMDb dataset from Hugging Face:

```python
from datasets import load_dataset
dataset = load_dataset("imdb")
```

---


```bash
pip install nltk spacy scikit-learn gensim datasets matplotlib seaborn
python -m spacy download en_core_web_sm
```

---

1. Clone the repository
2. Install dependencies
3. Run the main script or Jupyter Notebook:

```bash
python main.py
```

---



Input:

```
"This movie was amazing and emotional"
```

Output:

```
Top similar reviews with similarity scores
```

---



* Most frequent words highlight common themes in reviews
* Similarity search successfully retrieves related comments
* Word embeddings capture semantic meaning beyond keywords

---



* Use BERT embeddings for better semantic understanding
* Implement FAISS for scalable search
* Add clustering (KMeans) for grouping similar reviews
* Deploy as an API using Flask or FastAPI

---


This project demonstrates how raw text can be transformed into structured, meaningful data using NLP techniques.
The pipeline enables efficient semantic search, making it valuable for real-world applications like recommendation systems and customer feedback analysis.

---


