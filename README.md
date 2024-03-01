# KnowledgeHubRAG
Question answering RAG on pdf files

## Overview

**KnowledgeHubRAG** is a custom Question Answering (QA) system built on top of the Haystack framework. The system leverages the Retriever-Augmented Generation (RAG) pipeline to provide insightful and accurate answers to user queries on a set of provided PDF files.

## Features

- **Custom RAG Pipeline:** Utilizes a custom RAG pipeline built with Haystack to enhance question answering capabilities.

- **PDF Processing:** Extracts information from PDF files to build an index for efficient retrieval.

- **Language Models:** Incorporates pre-trained language models (LLM) to generate responses with context-awareness.
- 
### Key Components

#### 1. Haystack Framework
- Facilitates easy integration of the document store, retriever, and reader components.
- Provides efficient indexing and retrieval functionalities.

#### 2. FAISS Document Store
- An in-memory vector database used for fast and scalable document retrieval.

#### 3. Retriever (sentence-transformers)
- Converts queries and passages into embeddings for similarity searches.

#### 4. Reader (deepset/roberta-base-squad2)
- Performs reading comprehension on retrieved passages to identify answers.

#### 5. RAG Pipeline
- Combines the strengths of both Retriever and Reader for improved question answering.

## Usage

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/RAGenius.git

# Navigate to the project directory
cd KnowledgeHubRAG

# Install dependencies (make sure to use a virtual environment)
pip install -r requirements.txt
```
## Future Work and Potential Enhancements

While the current implementation provides a functional RAG pipeline for question answering on specific PDF data, there are several areas where further exploration and improvement could be considered:

1. **Training LLM on Specific PDF Data:**
   - Consider training a Language Model (LLM) on the specific domain of the PDF data to enhance context-awareness and improve the quality of generated answers.

2. **Incorporating Additional FAQs:**
   - Expand the training dataset for the retriever by incorporating additional Frequently Asked Questions (FAQs) relevant to the domain. This can help improve the retriever's ability to find relevant passages.

3. **Exploring Multiple Extractors:**
   - Experiment with different text extractors or parsers to handle diverse PDF layouts more effectively. This can enhance the robustness of the preprocessing step.

4. **Layout-Wise Parsing:**
   - Implement layout-aware parsing techniques to handle PDFs with complex structures and non-standard layouts. This can be particularly useful in domains where document layouts vary widely.

5. **Biomedical LLM Models:**
   - Explore and integrate pre-trained Language Models designed specifically for biomedical or scientific domains if your PDF data pertains to topics in the life sciences.

6. **Packaging for Deployment:**
   - Package the entire codebase using Docker to simplify deployment and scaling. Dockerizing the application can make it easier to manage dependencies and ensure consistent behavior across different environments.

7. **Scalability Considerations:**
   - Optimize the system for scalability by exploring distributed computing or parallel processing techniques. This can be crucial when dealing with a large number of documents or when aiming for real-time question answering.

8. **User Interface Development:**
   - Consider developing a user-friendly interface for interacting with the RAG pipeline. A graphical interface can facilitate easier usage for individuals who may not be familiar with command-line operations.

9. **Integration with Web Applications:**
   - Explore integration possibilities with web applications to provide a seamless experience for end-users. This could involve building a web-based frontend that interacts with the RAG pipeline.

10. **Logging and Monitoring:**
    - Implement logging and monitoring functionalities to keep track of system performance, errors, and usage patterns. This can aid in debugging and maintaining the system in a production environment.

