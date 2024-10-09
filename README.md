# AI LangChain SQL Agent

This project demonstrates how to use LangChain to build an AI agent that can query the Chinook database using SQL. The agent is powered by Azure OpenAI's GPT model and is configured to interact with a SQLite database of the Chinook digital media store.

## Project Overview

The main features of this project include:
- **Downloading the Chinook database**: The SQLite database file is downloaded from a given URL.
- **Connecting to the database**: The AI agent connects to the Chinook database to retrieve data.
- **Querying using LangChain**: An AI agent is created using LangChain with a custom prompt template for querying the Chinook database.
- **Azure OpenAI Integration**: The model is hosted on Azure OpenAI and accessed using API keys.

## Prerequisites

- **Python 3.9 or higher**
- **Azure OpenAI API keys** (Azure OpenAI subscription)
- **SQLite** installed or the ability to work with SQLite databases (bundled with Python)
- **Virtual Environment** (venv)

## Setup Instructions

### 1. Clone the repository

```bash
git clone <https://github.com/ridhwanashir/AI-Langchain-SQL-Agent>
cd AI-Langchain-SQL-Agent
```

### 2. Create a virtual environment

Create a virtual environment to isolate your project's dependencies:

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
```

### 3. Install dependencies

Install the necessary Python packages from requirements.txt:

```bash
pip install -r requirements.txt
```

### 4. Set up your environment variables

Create a `.env` file in the root of your project directory with the following content:

```env
AZURE_OPENAI_KEY=your_azure_openai_key_here
AZURE_OPENAI_ENDPOINT=your_azure_openai_endpoint_here
AZURE_OPENAI_API_VERSION=2023-03-15-preview  # or another version depending on your API
AZURE_OPENAI_DEPLOYMENT=your_azure_openai_deployment_name_here
```

Make sure to replace the placeholders with your actual Azure OpenAI credentials.

### 5. Running the agent

After setting up the environment and installing the dependencies, you can run the main script that builds and executes the AI agent with the rag_on_structured.ipynb

The AI agent will prompt you with the query result based on the Chinook database.

## Sample Usage

The example query used is:

```python
text_input = "album terlaris sepanjang masa."
```

The AI agent will generate SQL queries, execute them on the Chinook database, and return relevant results.

## Key Components

- **LangChain**: A framework for building applications with large language models.
- **Azure OpenAI**: A service for running OpenAI models on Azure infrastructure.
- **SQLite Database**: A lightweight SQL database engine used to store data from the Chinook database.

## License

This project is licensed under the MIT License.

## Additional Notes

1. Ensure that your `.env` file is added to `.gitignore` to avoid sharing sensitive API keys.
2. Adjust the `text_input` in the script for custom queries.
```

This markdown format provides a cleaner, more structured presentation of the README content, making it easier to read and understand.
