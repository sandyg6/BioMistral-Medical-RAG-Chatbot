# BioMistral Medical RAG Chatbot

## Project Overview

- **Goal**: Develop a chatbot to answer user queries about health concerns, symptoms, treatments, and more.
- **Purpose**: Serve as a reliable and accessible resource for medical information and advice.
- **Learning Context**: This project was completed as part of the learning stages of the [GUVI](https://www.guvi.in/) [SAWIT.AI](https://sawitnetwork.com/sawit-ai) Women-Only, Gen AI Learning Challenge.
  
## Key Components

1. **Llama Library**: Utilized for working with language models.
2. **Retriever**: Gathers context-relevant information to enhance LLM responses.
3. **Prompt Template**: Combines retriever results and user queries for accurate response generation.

# Technologies Used

- **Langchain**: For building the chatbot framework.
- **Hugging Face Transformers**: For implementing the LLM and embedding model.
- **PyPDF2**: For loading and parsing PDF documents.

## Implementation

- **Retrieval Augmented Generation (RAG) Chain**:
  - Integrates the retriever, LLM, and prompt template.
  - Facilitates dynamic retrieval and generation of medical information.
 
## Development Steps

### 1. Environment Setup
- Set up the development environment on Google Colab.
- Install required Python packages (Langchain, Sentence Transformers, Hugging Face, etc.).

### 2. Document Preprocessing
- Import medical documents into the project environment.
- Extract text using libraries like PyPDF2 for PDFs and `docx` for Word files.
- Utilize Langchain’s text splitter to chunk the text into manageable segments for retrieval.

### 3. Creating Embeddings and Vector Store
- Generate embeddings for text chunks using a pre-trained embedding model from Hugging Face.
- Create a **Chroma vector store** for efficient storage and retrieval of embeddings.
- Index text chunks with their corresponding embeddings for similarity search.

### 4. LLM Integration
- Load a pre-trained LLM using the Llama library for generating informative responses.
- Design a prompt template combining retrieved context and user queries.
- Construct a **Retrieval Augmented Generation (RAG) chain** using Langchain’s Chain Class to integrate the retriever, LLM, and prompt template.

## Testing
- Conducted testing with various medical-related prompts.

## Models and Data used
- https://huggingface.co/NeuML/pubmedbert-base-embeddings
- https://huggingface.co/MaziyarPanahi/BioMistral-7B-GGUF/tree/main
- https://www.nhlbi.nih.gov/files/docs/public/heart/healthyheart.pdf
