# JU Citizen's Charter Helpdesk Chatbot

JU Helpdesk Chatbot is an intelligent assistant designed to provide information about the Jahangirnagar University Citizen’s Charter services. It uses advanced natural language processing techniques to answer queries and provide accurate, concise responses.

## Features

- Query processing using semantic embeddings with **SentenceTransformer**.
- Fast and accurate similarity matching with **FAISS**.
- Handles typos and misspellings using **FuzzyWuzzy**.
- Query expansion with **WordNet** and custom synonyms.
- Interactive user interface built with **Streamlit**.
- Data backed by a **PostgreSQL** database.

## Requirements

- Python 3.12
- PostgreSQL database
- Required Python libraries (listed in `requirements.txt`)

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/MahinHossainMunna/HelpDeskChatbot.git
   cd HelpDeskChatbot
