# NLP-Powered Semantic Search Engine

An intelligent search engine for Machine Learning research papers, enhanced with an NLP-based Semantic Entity Type Classifier.

## Project Overview

This project uses Natural Language Processing and semantic embeddings to understand the meaning behind text rather than relying only on exact keyword matching.

The original system processes Machine Learning research papers and performs semantic search using vector embeddings.

As an additional feature, I implemented an NLP-based Semantic Entity Type Classifier that identifies the category of a technical or human-language entity.

## Added Feature: Semantic Entity Type Classification

The classifier can identify seven categories:

- Programming Language
- Human Language
- Software Library
- Software Framework
- Database System
- Operating System
- Development Tool

### Example Predictions

| Entity | Detected Type |
|---|---|
| Python | Programming Language |
| Hindi | Human Language |
| NumPy | Software Library |
| Django | Software Framework |
| PostgreSQL | Database System |
| Ubuntu | Operating System |
| Git | Development Tool |

## How It Works

The feature uses a Sentence Transformer model to convert entities and category descriptions into 384-dimensional semantic embeddings.

The classification pipeline is:

1. The user enters an entity such as `Django`.
2. The Sentence Transformer converts the entity into a vector embedding.
3. Predefined category descriptions are also converted into embeddings.
4. Similarity is calculated between the entity embedding and each category embedding.
5. The category with the highest semantic similarity is returned as the predicted entity type.

## Model Used

`sentence-transformers/all-MiniLM-L6-v2`

This model was selected because it provides efficient and meaningful semantic representations of text.

## Example Output

```text
Entity: Django
Detected Type: Software Framework
Similarity Score: 0.4494# CBSOT_Project-2
