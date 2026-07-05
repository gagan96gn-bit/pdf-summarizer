# PDF Summarizer

An automated pipeline that extracts text from PDF documents, generates abstractive summaries, and scores the output for readability.

## Overview
Takes any uploaded PDF, extracts and cleans the text, summarizes it using a transformer model, and reports readability metrics on the source document.

## Approach
- **Text extraction:** pdfplumber, page-by-page
- **Text cleaning:** regex-based whitespace and character normalization
- **Summarization:** Hugging Face `facebook/bart-large-cnn`, with sentence-aware chunking for long documents
- **Readability scoring:** Flesch Reading Ease, average sentence length, lexical diversity (via textstat and NLTK)

## Sample output
On a test document (EU circular economy policy PDF): readability score 17.74, average sentence length 19.6 words, lexical diversity 0.23.

## Tools
Python, pdfplumber, Hugging Face Transformers (BART), NLTK, textstat

## How to run
1. Open the notebook in Google Colab
2. Upload a PDF when prompted
3. Run cells sequentially — extraction, cleaning, summarization, readability metrics
