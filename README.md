# Symantic Spotter using LlamaIndex

This project implements a **Semantic Spotter** using LlamaIndex (formerly GPT Index) and OpenAI’s GPT-3.5 model. It is designed to provide accurate responses to insurance-related queries by combining large language models with vector-based search for efficient and relevant answers.

## Table of Contents
- [Project Overview]
- [Key Features]
- [Prerequisites]
- [Installation]
- [How to Run the Symantic Spotter]
- [Architecture]
- [Improvements]
- [Challenges]
- [Future Enhancements]
- [License]

## Project Overview
The Symantic Spotter provides a question-answering system for insurance policies using a combination of document retrieval and generative models. It indexes documents, retrieves relevant passages, and uses AI-powered re-ranking to improve the accuracy of responses.

## Key Features
- **Document Retrieval**: Indexes and retrieves relevant insurance documents.
- **Response Generation**: Utilizes GPT-3.5 to generate answers based on document content and external knowledge.
- **Query Re-Ranking**: Enhances response relevance with Cohere’s re-ranking.
- **Caching**: Stores frequent responses for quick retrieval.
- **Customizable Prompting**: Allows custom prompt templates for better alignment of answers with document context.

## Prerequisites
1. **Install Required Libraries**: Ensure all necessary libraries are installed. Run all cells that install dependencies and code.
2. **Prepare Dataset**: Organize your dataset of insurance documents in the specified directory.



