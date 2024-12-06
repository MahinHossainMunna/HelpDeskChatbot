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
   git clone https://github.com/MahinHossainMunna/HelpDeskChatbot.git
   cd HelpDeskChatbot
2. **Set Up Virtual Environment**:

python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
Install Dependencies:

pip install -r requirements.txt
Set Up PostgreSQL:

Create a PostgreSQL database named ju_chatbot.
Import the provided database schema (schema.sql) and data.

psql -U your_username -d ju_chatbot -f schema.sql
Build FAISS Index: Ensure your PostgreSQL database is populated and run the following command to build the FAISS index:


python build_index.py
Run the Chatbot: Start the chatbot using Streamlit:


streamlit run app.py
Access the Chatbot: Open the browser and navigate to http://localhost:8501.

##Project Structure

JU-Helpdesk-Chatbot/
├── app.py                 # Main Streamlit application
├── build_index.py         # Script to build the FAISS index
├── requirements.txt       # Python dependencies
├── schema.sql             # PostgreSQL database schema
├── data/
│   └── JUdb.xlsx          # Original dataset in Excel
├── train/
│   ├── faiss_index.bin    # FAISS index file
│   └── saved_model        # Trained SentenceTransformer model
├── images/
│   └── julogo.png         # University logo for UI
└── README.md              # Project documentation

##Technologies Used
Streamlit: Interactive front-end interface.
SentenceTransformer: Semantic embedding for text processing.
FAISS: Nearest neighbor search for fast query matching.
FuzzyWuzzy: Fuzzy matching for handling typos.
NLTK WordNet: Query expansion with synonyms.
PostgreSQL: Relational database for data storage.

##Contributing
Contributions are welcome! Please open an issue or submit a pull request if you would like to suggest an improvement.

##License
This project is licensed under the *MIT* License. See the LICENSE file for more details.

*Developed by*: **Md. Mahin Hossain Munna**
*Supervised by*: **Dr. M Shamim Kaiser**
