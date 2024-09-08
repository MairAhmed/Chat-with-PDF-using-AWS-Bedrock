# Chat-with-PDF-using-AWS-Bedrock

This is a Streamlit app that allows users to ask questions about PDF documents, leveraging the power of AWS Bedrock's Titan Embeddings Model for document embedding and retrieval. The app supports querying PDF documents, processing them into vector embeddings using FAISS, and answering user questions with various LLMs such as Claude and Llama2.

# Features
# Document Ingestion:
Load PDFs from a directory and split the text into manageable chunks.
# Vector Store:
Create and update a FAISS vector store using embeddings generated from the Titan model.
# Question Answering:
Utilize Bedrock LLMs (Claude and Llama2) to answer questions based on context from the ingested PDFs.
# LLM Integration:
Integrates with Claude and Llama2 models via AWS Bedrock.
# Real-time Interaction:
Ask questions from PDFs in real-time and receive accurate answers based on the content.

# Installation
Clone the repository:

git clone https://github.com/your-repo/your-app.git

cd your-app

# Install the required dependencies:
pip install -r requirements.txt

Set up your AWS credentials to access Bedrock.

# Usage
Run the App:

streamlit run app.py

Ingest PDFs:

Add PDF files to the data directory.

Use the sidebar to update or create the FAISS vector store from the PDF documents.

Ask Questions:

Input your question related to the PDF files into the main text input box.

Click on "Claude Output" or "Llama2 Output" to get answers generated by the respective LLMs.

# Key Components
# Data Ingestion
# PyPDFDirectoryLoader: 
Loads and parses PDF documents from a given directory.
# Text Splitter:
Uses Recursive Character Text Splitter to break down large documents into manageable chunks.
# Vector Embeddings
# FAISS:
Stores document embeddings for efficient retrieval during question-answering.
# Bedrock Titan Embeddings:
Uses the Titan embeddings model from AWS Bedrock to convert text into vector embeddings.
# Question-Answering
# RetrievalQA:
Chain that takes a query and retrieves the most relevant chunks from the vector store, feeding them into a pre-trained LLM for the final response.

# Language Models
# Claude (Anthropic): 
Uses the Claude model (ai21.j2-mid-v1) via Bedrock for question answering.
# Llama2 (Meta): 
Integrates the Llama2-70B model via Bedrock for detailed responses.
# Environment Variables
Set up your AWS credentials to access Bedrock services.




