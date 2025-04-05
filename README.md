# Local AI Agent
---

# Restaurant Review Q&A System

This project implements a simple question-answering system using Langchain and Ollama, built following a tutorial by Tech With Tim. It allows users to ask questions about a pizza restaurant, and the system responds by retrieving relevant reviews and providing answers based on the context of those reviews.

## Features
- **Review Data**: Uses a CSV file of restaurant reviews, including titles, review content, ratings, and dates.
- **Vector Embeddings**: Embeds review data using Ollama's embeddings for efficient retrieval.
- **Chroma Vector Store**: Stores embedded reviews and allows for fast similarity-based search.
- **Question Answering**: Uses Langchain's prompt templates and Ollama's model to generate answers based on relevant reviews.

## Tech Stack
- **Langchain**: A framework for building NLP pipelines.
- **Ollama**: A machine learning library for generating and handling embeddings and language models.
- **Chroma**: A library for managing vector databases and similarity search.
- **Python**: The primary programming language used.
- **Pandas**: Used to handle the restaurant reviews data from a CSV file.

## Installation

To get started, you’ll need Python 3.8+ installed. Then, clone the repository and install the required dependencies.

```bash
git clone <repository_url>
cd <repository_folder>
pip install -r requirements.txt
```

You'll also need to download or have access to the `realistic_restaurant_reviews.csv` file, which should be placed in the root directory of the project.

## Usage

1. **Run the Vector Store Setup**:  
   First, ensure your vector store is set up by running the `vector.py` script. This will embed and store restaurant reviews in a Chroma database.

```bash
python vector.py
```

2. **Ask Questions**:  
   Once the database is set up, you can run the `main.py` script to start asking questions.

```bash
python main.py
```

   You can type questions about the pizza restaurant, and the system will respond with answers based on the most relevant reviews. To quit, type `q`.

## Example

1. Start the application by running `main.py`.
2. Ask questions such as:
   - "What are the best dishes at this restaurant?"
   - "What do customers think about the service?"

The system will fetch the relevant reviews from the database and generate an answer based on those reviews.

## Files
- `vector.py`: This script handles loading the CSV data, embedding the reviews, and storing them in a vector database (Chroma).
- `main.py`: This script allows users to interact with the system by asking questions and receiving answers based on relevant restaurant reviews.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

