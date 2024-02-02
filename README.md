# Generating Embeddings using Universal Sentence Encoder(USE),TensorFlow-Hub(TF-Hub) and GloVe models

## Table of Contents
- [Introduction](#introduction)
- [Methodologies Implemented](#methodologies-implemented)
  - [CSV Data](#csv-data)
    - [Import Libraries](#import-libraries)
    - [Loading CSV Data](#loading-csv-data)
    - [Loading the Pre-Trained Model for CSV Data (USE)](#loading-the-pre-trained-model-for-csv-data-use)
    - [USE Embeddings for a Text](#use-embeddings-for-a-text)
    - [Generating Embeddings](#generating-embeddings)
  - [JSON Data](#json-data)
    - [Import Libraries](#import-libraries) 
    - [Loading JSON Data](#loading-json-data)
    - [Loading the Pre-Trained Model for JSON Data](#loading-the-pre-trained-model-for-json-data)
    - [Text Preprocessing](#text-preprocessing)
    - [Generating Embeddings for JSON Data](#generating-embeddings-for-json-data)
    - [Convert the Embedded Vectors to Save in JSON Forms](#convert-the-embedded-vectors-to-save-in-json-forms)
    - [Retrieving from the Saved File](#retrieving-from-the-saved-file)
- [Code Execution](#code-execution)
- [Usage](#usage)
- [Conclusion](#conclusion)

## Introduction
  This document outlines two projects: one using TensorFlow-Hub(TF-Hub) and Universal Sentence Encoder(USE) for embeddings from a CSV file, and another using GloVe for embeddings from a JSON file. The resulting embeddings are processed and stored for versatile use in natural language processing tasks.

## Methodologies Implemented:
### CSV Data:
- **Import Libraries**:
  -Import the Necessary libraries 
- **Loading CSV Data**:
  - The CSV data containing text lines is loaded into a pandas DataFrame. The file path is specified, and the CSV data is read into the `dataset` variable.
- **Loading the Pre-Trained Model for CSV Data (USE)**:
  - The Universal Sentence Encoder (USE) is specifically designed for generating embeddings from sentences. It transforms variable-length text inputs into fixed-size vectors, commonly referred to as embeddings, that capture semantic information about the input sentences. 
- **USE Embeddings for Text**:
  -The implemented function, get_use_embeddings, showcases a streamlined approach to harnessing the power of the Universal Sentence Encoder (USE) for text embedding generation. 
- **Generating Embeddings**:
  -  Generating embeddings for a CSV file unfolds seamlessly through the integration of the Universal Sentence Encoder (USE). Leveraging TensorFlow and TensorFlow Hub, this methodology facilitates the transformation of textual data within the CSV into high-dimensional vectors, encapsulating semantic information. 

### JSON Data:
- **Import Libraries**:
  -Import the Necessary libraries 
- **Loading JSON Data**:
  - The JSON data containing textual entries is loaded from the specified file path into the Python environment using the `json.load()` function.
- **Loading the Pre-Trained Model for JSON Data**:
  - The GloVe (Global Vectors for Word Representation) model is a pre-trained word embedding model. Pre-training involves training the model on a large corpus of text data to learn vector representations (embeddings) for words based on their semantic relationships.
- **Text Preprocessing**:
  - Text preprocessing is performed using the `simple_preprocess()` function from Gensim. This step tokenizes the text and performs basic preprocessing tasks such as lowercasing and punctuation removal.
- **Generating Embeddings for JSON Data**:
  - Word embeddings are generated for the preprocessed text using the pre-trained GloVE model. The embeddings capture the semantic meaning of words in a continuous vector space.
- **Convert the Embedded Vectors to Save in JSON Forms**:
  -This process involves converting embedded vectors into a JSON format, facilitating efficient storage and retrieval. The script employs the json module to serialize embedded vectors, providing a versatile and structured representation for further use in various applications.
- **Retrieving from the Saved File**:
  -To retrieve embedded vectors from the saved JSON file, a simple script utilizing Python's json module is employed, allowing seamless integration and utilization of previously stored embeddings for downstream tasks. 


## Code Execution:
The code iterates through each line in the CSV dataset or extracts text from the JSON data and generates embeddings using the appropriate model or methodology, and prints the embeddings for each line or entry.

## Usage:
- To use the code:
  1. Ensure to install the necessary libraries using `pip` command.

  ```
  !pip install tensorflow tensorflow-hub
  !pip install spacy
  !python -m spacy download en_core_web_md
  !pip install spacy spacy-transformers
  ```

  2. Provide the path to the CSV file containing the text data or the JSON file with textual entries.
  3. Run the code to generate embeddings for each line or entry in the dataset.
  4. For CSV data Universal Sentence Encoder(USE) model is used. You can download it using this [drive link.] 
     https://tfhub.dev/google/universal-sentence-encoder/4

## Conclusion:
- These projects demonstrate how to leverage pre-trained language models like TF-Hub and GloVe to generate embeddings for textual data from both CSV and JSON formats. Embeddings capture the semantic meaning of text and can be used as input features for various downstream NLP tasks.
