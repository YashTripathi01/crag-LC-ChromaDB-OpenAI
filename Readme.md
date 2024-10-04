# RAG QA Bot - Retrieval Augmented Generation

This application implements a **Retrieval-Augmented Generation (RAG)** model using OpenAI's GPT-2 Opensource model. It is designed to respond to user queries by first retrieving relevant documents and then generating a context-aware answer. LangChain is used to enhance the interaction with LLMs, and prompt templates are integrated for improving performance and accuracy.

## Features

-   Vector-based document retrieval.
-   Generative answers using **OpenAI's GPT-2 model**.
-   **LangChain** integration for more sophisticated LLM handling.
-   Flexible and dynamic prompt templates for improved responses.

## Table of Contents

-   [Prerequisites](#prerequisites)
-   [Installation](#installation)
-   [Integrating LangChain](#integrating-langchain)
-   [Working with Prompt Templates](#working-with-langchain-prompt-templates)
-   [Running the Notebook](#running-the-notebook)

## Prerequisites

Before you start, make sure you have the following:

1. **Python 3.10+** installed.
2. **Git** for version control.

## Installation

1. Clone the repository to your local machine:

    ```bash
    git clone https://github.com/your-username/rag-qa-bot.git
    cd rag-qa-bot
    ```

2. Create a virtual environment and activate it:

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:

    ```bash
    pip install ipykernel
    ```

4. Add the virtual environment to kernel list:

    ```bash
    python3 -m ipykernel install --user --name=venv
    ```

## Integrating LangChain

LangChain helps to build chains of calls to LLMs and supports more complex workflows than a single OpenAI prompt. This project uses LangChain to enhance interaction with OpenAI's GPT-2 and manage the prompt construction dynamically.

## Working with LangChain Prompt Templates

Prompt templates are a crucial part of the RAG system because they structure how the model interacts with the retrieved documents and user query.

### Benefits of Prompt Templates:

-   **Contextual Awareness**: By providing a structured format where the context (retrieved documents) and the query are combined, the LLM understands the question in the correct domain.
-   **Customizability**: Prompt templates allow you to dynamically change input variables, like the user query or the retrieved context.
-   **Improved Accuracy**: Well-designed prompts lead to more accurate and coherent responses, as the system can understand the broader context instead of just responding to isolated queries.

**Example of a Prompt Template in Action:**

```python
template = """
You are an expert customer support agent.

Context: {context}

Based on the above context, answer the following question:
Question: {question}

Answer:
"""
```

By using such templates, the model can frame its responses more accurately, factoring in both the context and the specific question asked.

### How Prompt Templates Improve Performance

1. **Consistency**: The model’s responses are consistent since the prompt structure remains the same.
2. **Clarification**: The prompt guides the model on how to respond (e.g., as an expert in customer support), improving the relevance of answers.
3. **Adaptability**: You can easily adapt the prompt template for different use cases (e.g., tech support, sales inquiries) without changing the core logic.

## Running the Notebook

1. Open the notebook in your favorite environment, such as Jupyter or Google Colab.

2. Execute all the cells sequentially.

---

This guide should help you get started with the RAG QA bot with LangChain enhancing the overall architecture and performance.
