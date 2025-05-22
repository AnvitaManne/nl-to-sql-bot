# Natural Language to SQL Chatbot

This project is a command-line chatbot that converts natural language queries into SQL queries to interact with a travel booking database. It uses a Planner-Executor architecture with OpenAI's GPT models and SQLite.


## Features

- Converts user queries in plain English to SQL.
- Executes generated SQL on a real travel database (`travel2.sqlite`).
- Supports simple and complex queries (e.g., flights, hotels, bookings).
- Includes a local city-to-airport mapping for fast resolution.
- Modular design: planner, executor, and chat interface are separated.


## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/nl-to-sql-chatbot.git
cd nl-to-sql-chatbot
````

### 2. Download the Database

Download the SQLite database and place it in the project directory:

[travel2.sqlite](https://storage.googleapis.com/benchmarks-artifacts/travel-db/travel2.sqlite)

### 3. Install Dependencies

```bash
pip install --upgrade --force-reinstall pydantic pydantic-core openai
```

### 4. Set OpenAI API Key

In your script or environment:

```python
openai.api_key = "sk-..."
```


## Usage

Run the chatbot:

```bash
python chatbot.py
```

Sample input:

```
Show me all flights from Delhi
```

Sample output:

```
Generated SQL: SELECT * FROM flights WHERE departure_airport = 'DEL';
Results: (first 10 rows shown)
```


## Technologies Used

* Python 3
* SQLite
* OpenAI GPT (e.g., GPT-4o)
* Pydantic


## Author

Anvita Manne
