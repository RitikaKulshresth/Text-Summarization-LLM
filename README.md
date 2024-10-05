**PDF Text Summarization with Embedding-Based Similarity Search Overview**


This project demonstrates an end-to-end pipeline for extracting text from multiple PDFs,
generating vector embeddings using the sentence-transformers/all-MiniLM-L6-v2 model, and performing similarity search to retrieve and summarize the most relevant content.
It utilizes tools like LangChain, Hugging Face Embeddings, and FAISS for vector search, allowing for quick and accurate retrieval of answers from a collection 
of business documents.

**Key Features**

PDF Text Extraction: Extracts content from PDF files using LangChain's PyPDFLoader.
Embedding Generation: Converts extracted text into vector embeddings using the HuggingFaceEmbeddings model sentence-transformers/all-MiniLM-L6-v2.
Vector Search with FAISS: Indexes the vector embeddings using FAISS and retrieves the most relevant documents based on cosine similarity.
Query-Based Similarity Search: Retrieves top relevant documents from the indexed collection for any input query.
Text Summarization: Summarizes the top relevant documents using transformers summarization models, generating concise insights from large texts.

**Technologies Used**

LangChain: For chaining tasks like text extraction and retrieval.
Hugging Face Transformers: For embedding generation and text summarization.
FAISS: For efficient similarity-based search on high-dimensional vector data.
Google Colab: To run the entire pipeline in a cloud-based environment.

**Project Steps**

PDF Upload and Extraction:

PDFs are uploaded, unzipped, and extracted using PyPDFLoader.
Non-empty text is stored for further processing.
Embedding Generation:

Text content is converted into vector embeddings using HuggingFaceEmbeddings.
Vector Store Creation:

Embeddings are stored in a FAISS index for efficient similarity search.
Similarity Search:

A RetrievalQA system is built to retrieve the most relevant documents based on cosine similarity.
The query used to search is customizable, and the top k results are fetched from the indexed documents.
Text Summarization:

The content of the retrieved documents is summarized using the transformers library to provide concise, relevant information.


**Usage**

Setup Hugging Face API: Ensure you have your Hugging Face API token set up for model access.
Upload PDF Files: Upload and extract your PDF documents into a folder.
Run the Pipeline: Execute the provided Colab code to extract text, generate embeddings, perform similarity search, and get summarized results.
Custom Queries: Input your own queries to retrieve and summarize relevant document sections.

**Example Query**

Input Query: "What is Multi-Head Attention?"

**How to Run**

Clone this repository to your local environment or Google Colab.
Upload the required PDF documents into the specified folder.
Run the notebook to process the documents, generate embeddings, and perform similarity search and summarization.

Retrieves the top 2 relevant documents containing information on Multi-Head Attention.
Summarizes the content to provide a concise explanation.

**How to Run**
Clone this repository to your local environment or Google Colab.
Upload the required PDF documents into the specified folder.
Run the notebook to process the documents, generate embeddings, and perform similarity search and summarization.
