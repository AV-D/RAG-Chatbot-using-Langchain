# RAG-Chatbot-using-Langchain

This repository contains two Jupyter notebooks (`Part_A.ipynb` and `Part_B.ipynb`) that are part for building advanced chatbots using LangChain, OpenAI, and Pinecone vector DB with Retrieval Augmented Generation (RAG).

#### Part A: Code Understanding Model

**Objective**: Develop a chatbot capable of understanding and responding based on the context provided from code files.

**Key Features**:
- Utilizes LangChain and OpenAI's GPT-3.5-turbo model.
- Integrates with Pinecone to manage the vector database for storing and retrieving knowledge.
- Demonstrates basic chat functionalities without RAG.

**Installation**:
Ensure you have Python installed and then run:
```bash
pip install -qU langchain==0.0.354 openai==1.6.1 datasets==2.10.1 pinecone-client==3.1.0 tiktoken==0.5.2
```

**Usage**:
1. Set up environment variables for OpenAI and Pinecone API keys.
2. Execute the cells sequentially to initialize the chatbot, load data, and interact with the chatbot.

#### Part B: Custom Data Chatbot

**Objective**: Extend the chatbot from Part A to answer questions based on custom data from multiple documents using RAG.

**Key Features**:
- Builds upon the initial chatbot by incorporating custom data handling.
- Uses LangChain for seamless integration of different components.
- Demonstrates the ability to remember and summarize conversations.

**Installation**:
Use the same installation steps as in Part A.

**Usage**:
1. Similar to Part A, ensure all API keys are set.
2. Run the notebook cells to initialize the chatbot with RAG capabilities.
3. Interact with the chatbot to see responses based on the loaded custom data.

**Contributing**:
Contributions to improve the chatbot or extend its capabilities are welcome. Please ensure to follow the existing code structure and submit a pull request for review.

**Documentation**:
For more detailed information on the libraries and APIs used, refer to:
- [LangChain Documentation](https://langchain.com)
- [OpenAI API Documentation](https://platform.openai.com/docs/)
- [Pinecone Documentation](https://www.pinecone.io/docs/)

**Changelog**:
- Initial release: Basic chatbot functionalities.
- Update 1: Integration of custom data and RAG.

For any issues or further queries, please open an issue in this repository.

# Theoritical Background

### 1. Retrieval-Augmented Generation (RAG)
RAG is a framework that enhances the capabilities of large language models (LLMs) by combining them with a retrieval system. The idea is to prevent the model from "hallucinating" or generating factually incorrect information by providing it with access to a relevant knowledge base during the generation process. This is particularly useful when dealing with questions or topics not covered in the model's training data.

- **How it works**: When a query is received, the system first retrieves relevant documents or data snippets from a knowledge base (using vector similarity search, for example). These retrieved pieces are then fed into the LLM along with the query to generate an informed and accurate response.

### 2. LangChain
LangChain is a library designed to facilitate the building of language applications, particularly those that integrate with other systems like databases or other APIs. It provides tools and abstractions to handle various components of language AI applications, including retrieval systems, language models, and workflows combining both.

- **Usage in RAG**: In the context of RAG, LangChain can manage the workflow where data is retrieved from a database and then passed to an LLM for response generation.

### 3. OpenAI's Language Models
OpenAI offers several powerful language models, such as GPT-3 and GPT-3.5, which are capable of understanding and generating human-like text based on the input they receive. These models are trained on diverse internet text and can perform a wide range of text-based tasks.

- **Role in RAG**: In a RAG setup, OpenAI's models are used to generate responses based on both the input query and the context provided by the retrieved documents.

### 4. Pinecone
Pinecone is a vector database designed for machine learning applications. It allows users to store vector embeddings and perform efficient similarity searches. This is crucial for applications like RAG, where quick retrieval of relevant information based on vector similarity is needed.

- **Integration in RAG**: Pinecone acts as the storage and retrieval backbone. It stores vector representations of data and retrieves the most relevant vectors in response to queries from the LLM.

### 5. Vector Embeddings
Vector embeddings are high-dimensional representations of data (text, images, etc.) that capture the semantic meaning of the input in a way that can be processed by algorithms. In the context of RAG, embeddings of text documents are used.

- **Purpose**: Embeddings allow the system to perform semantic similarity searches. For instance, embeddings can be used to find the most relevant documents to a user's query before generating a response.

### 6. API Keys and Environment Setup
To use services like OpenAI and Pinecone, you need to have API keys which authenticate your requests to these services. Setting up the environment correctly with these keys is crucial for the secure and efficient operation of your application.

For more detailed guidance on building such systems, you can refer to the Pinecone documentation on building a RAG chatbot [here](https://docs.pinecone.io/guides/get-started/build-a-rag-chatbot).
