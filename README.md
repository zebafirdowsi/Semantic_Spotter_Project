# Semantic Spotter
## Overview
This project implements a Q&A system that answers user queries regarding insurance policies by utilizing **RAG with LlamaIndex** and **OpenAI’s GPT-3.5-turbo**. The system retrieves relevant document sections and generates precise answers using a Retrieval-Augmented Generation (RAG) approach. To optimize performance, a caching mechanism is implemented to store answers for frequently asked questions.

## Dataset Description
The dataset comprises various insurance documents in `.pdf` and `.docx` formats, which contain information about:
- **Policyholder details**
- **Nominee conditions**
- **Policy benefits and claims**
- **Exclusions and limitations**

These documents are used as the knowledge base for answering user queries.

## Methodology

### Step 1: Data Loading and Preprocessing
- **File Formats**: The system handles document loading using **SimpleDirectoryReader**, which processes and reads text from documents.
- **Document Parsing**: Text is processed and split into manageable chunks for indexing and retrieval.
  
### Step 2: Indexing and Query Engine Setup
- **LlamaIndex**: The parsed documents are indexed using **VectorStoreIndex** from LlamaIndex, allowing efficient retrieval of relevant document sections.
- **Query Engine**: A query engine is created using the indexed documents, which can be queried to extract relevant information based on user inputs.

### Step 3: LLM Integration (OpenAI GPT-3.5-turbo)
- **LLM for Responses**: **OpenAI’s GPT-3.5-turbo** model is used to generate human-like answers based on the retrieved document sections. The model is invoked through the OpenAI API.
- **Custom Prompting**: Custom prompts are provided to the language model to ensure that responses are contextual and accurate.
  
### Step 4: Caching with Diskcache
- **Response Caching**: A **disk-based cache** is implemented to store the results of frequently asked questions, reducing response time for similar future queries.

## Model Building and Evaluation

1. **LlamaIndex Query Engine**:
   - Used to index documents and retrieve context for queries.
   - Ensures relevant document sections are fetched efficiently.

2. **GPT-3.5-turbo Integration**:
   - Model used to generate precise and contextually accurate answers.
   - Custom prompt templates are utilized to refine the responses.

3. **Diskcache Implementation**:
   - Used to store answers to common queries, which boosts the system's performance.

## Results and Evaluation

- The system successfully answers user queries by retrieving relevant sections of insurance documents and generating accurate, context-aware responses.
- The caching mechanism reduces response times for frequently asked questions.

## Dependencies
- `llama-index`: For document indexing and query engine setup.
- `openai`: For integrating the OpenAI GPT models.
- `diskcache`: For implementing response caching.


