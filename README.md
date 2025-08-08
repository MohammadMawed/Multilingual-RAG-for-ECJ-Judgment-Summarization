# Multilingual RAG for ECJ Judgment Summarization

This repository contains two Jupyter notebooks implementing multilingual summarization systems for European Court of Justice (ECJ) judgments. The goal is to generate high-quality summaries in German and English using retrieval-augmented strategies that leverage the structure of legal documents and their multilingual alignment.

## Overview

The summarization pipelines are designed to evaluate whether combining multiple language versions of the same legal text improves the quality of generated summaries. The systems operate on preprocessed pairs of ECJ decisions available in the EUR-Lex dataset.

### 1. Baseline RAG (Organic Approach)

The baseline system applies a standard retrieval-augmented generation method using multilingual embeddings and FAISS-based chunk retrieval. Summaries are generated from the top-k retrieved chunks without further synthesis or ranking.

- Notebook: `organic_multilingual_rag_ecj.ipynb`

### 2. SCaLAR-Inspired Hierarchical RAG

This system follows a three-stage architecture inspired by hierarchical summarization techniques. It includes:

- Micro-level summarization of chunks  
- Global summary synthesis from micro-summaries  
- Final re-ranking using semantic similarity (Legal-BERT)

- Notebook: `scalar_multilingual_rag_ecj.ipynb`

## Evaluation

The notebooks include integrated evaluation using the following metrics:

- **ROUGE-1**, **ROUGE-2**, **ROUGE-L**: to measure lexical overlap  
- **BERTScore (F1)**: to assess semantic similarity

Both systems are tested on a sample of ECJ decisions with available reference summaries.

## Usage

Each notebook is self-contained. To run:

1. Open the notebook in Jupyter or VS Code.  
2. Follow the execution order (sections are labeled).  
3. Adjust paths to document files, models, or output directories as needed.  
4. Run the final evaluation cells to view the results.

## Project Context

This repository was created as part of the **Project Seminar Data Science and Artificial Intelligence 2025** to support multilingual summarization research for ECJ legal texts. The project was developed under the supervision of **Bianca STEFFES**.
