# NLP: Text Representation, Similarity and Word Embeddings

## Project Overview

This project explores fundamental Natural Language Processing (NLP) techniques using real-world news articles from BBC News.

The project focuses on comparing different text representation methods, measuring text similarity and distance, and implementing a simplified Word2Vec model using a neural network to learn word embeddings.

## Dataset and Data Source

- **Data Source:** BBC News
- **Number of Articles:** 4
- **Data Type:** Unstructured textual data
- **Data Collection Method:** Web scraping using Goose3

Four BBC news articles were extracted from their original URLs using the Goose3 Python library.

**Original article URLs:**

1. https://www.bbc.com/news/articles/c39eprxln0go
2. https://www.bbc.com/news/articles/cvgxjn92x9jo
3. https://www.bbc.com/news/articles/cr7kmlg0lxpo
4. https://www.bbc.com/news/articles/cdewx6rew04o

*Note: The original articles are third-party content. This repository contains the code for extracting and analysing the text rather than redistributing the full articles.*

## Key Features and Methodologies

### 1. Text Representation

Explored two common approaches for converting text into numerical representations:

- **Bag-of-Words (CountVectorizer):** Represents documents based on word frequency.
- **TF-IDF (TfidfVectorizer):** Assigns weights to words based on their importance across documents.

### 2. Text Similarity and Distance Measurement

Applied different distance metrics to investigate similarities and differences between news articles:

- Edit Distance
- Binary Distance
- Jaccard Distance
- Masi Distance
- Euclidean Distance

Also performed basic vector operations, including addition, subtraction and squared Euclidean distance calculations.

### 3. Text Preprocessing and Vocabulary Extraction

Performed text preprocessing to prepare the articles for word embedding training:

- Converted text to lowercase.
- Removed punctuation.
- Normalised whitespace.
- Tokenised text into individual words.
- Extracted unique vocabulary using Python sets.

### 4. Word2Vec Implementation

Implemented a simplified Skip-gram-style Word2Vec neural network using TensorFlow.

Key steps included:

- Created word-to-integer mappings.
- Generated context word pairs using a sliding window approach.
- Converted words into one-hot encoded vectors.
- Constructed a neural network with input and output weight matrices.
- Applied softmax activation and cross-entropy loss.
- Trained the model using gradient descent.
- Extracted two-dimensional word embeddings from the trained network.

### 5. Word Embedding Visualisation

Used Matplotlib to visualise the learned word embeddings in a two-dimensional scatter plot.

The visualisation provides an overview of how words are represented in the embedding space based on their contextual relationships.

## Technologies and Libraries

- Python
- Goose3
- Scikit-learn
- NLTK
- NumPy
- Pandas
- TensorFlow
- Matplotlib

## Project Structure

```text
NLP-Text-Representation-and-Word-Embeddings/
│
├── README.md
├── requirements.txt
│
├── notebooks/
│   └── NLP_Analysis.ipynb
│
└── images/
    └── word_embeddings.png
```

## Learning Outcomes

Through this project, I gained practical experience in:

- Extracting and processing unstructured textual data.
- Understanding Bag-of-Words and TF-IDF representations.
- Applying different text similarity and distance metrics.
- Understanding context windows and word co-occurrence.
- Implementing a simplified Skip-gram neural network.
- Learning how neural networks generate word embeddings.
- Visualising word relationships in a low-dimensional space.

## Future Improvements

- Expand the dataset with more news articles.
- Experiment with different context window sizes and embedding dimensions.
- Compare the custom implementation with established Word2Vec implementations.
- Explore more advanced word embedding and NLP techniques.
