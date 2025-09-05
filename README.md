# Search Engine
*Search Engine Project*

This project implements a mini search engine in three phases, progressing from raw document parsing to query ranking and evaluation using a vector space model.

*Overview*

The system processes the FT911 news dataset, cleans and structures the data, builds an inverted index, and then ranks search results using TF-IDF and cosine similarity. The final output is formatted according to TREC standards for evaluation with relevance judgments.

*Project Structure*
Phase	Notebook	Description
'Phase 1'	parses and preprocesses the raw FT911 documents by cleaning text, tokenizing, removing stopwords, and applying stemming. Produces structured outputs, including a forward index and document mapping files.
'Phase 2'	builds the inverted index, mapping each term to a sorted list of documents containing it, along with term frequencies for TF-IDF computation.
'Phase 3'	implements a vector space model to process queries, calculate TF-IDF scores, rank documents using cosine similarity, and generate TREC-formatted output for evaluation.
Workflow

####Phase 1 – Data Preparation

Load and clean the FT911 dataset.
Tokenize, remove stopwords, and apply Porter stemming.
Generate structured files for indexing.

####Phase 2 – Indexing

- Build an inverted index from the preprocessed data.
- Store postings lists sorted by document IDs.
- Prepare for fast query lookups.

####Phase 3 – Query Processing

- Compute TF-IDF weights for terms and documents.

- Process queries and rank documents using cosine similarity.

- Output results in TREC format for evaluation using main.qrels.

- Output Format

- The final ranked results follow TREC’s fixed-width tab-separated format:

TOPIC    DOCUMENT    UNIQUE#    COSINE_VALUE


Example:
001    FT911-14    1    0.6532
001    FT911-15    2    0.6127

Technologies Used

Python
Jupyter Notebook
Porter Stemmer
TF-IDF Weighting
CosineSimilarity
TREC Evaluation Standards

