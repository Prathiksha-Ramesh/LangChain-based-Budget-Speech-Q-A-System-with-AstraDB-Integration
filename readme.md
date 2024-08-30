# LangChain-based Budget Speech Q&A System with AstraDB Integration

This project is a Python application that leverages LangChain components and Hugging Face datasets to create a document question-and-answer (Q&A) system. The application integrates with AstraDB for vector storage, making it possible to retrieve and query large datasets efficiently. It specifically focuses on querying the 2024-2025 Budget Speech of India.

## Project Structure
```
project-directory/
 │ ├── app.py 
 ├── requirements.txt 
 ├── .env 
 ├── README.md 
 ├── LICENSE 
 ├── .gitignore 
 ├── Budget_Speech.pdf 
 └── notebook.ipynb
```
 
## Getting Started

### Prerequisites

Ensure you have the following installed:
- Python 3.8 or higher
- Pip (Python package installer)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/langchain-qa-astradb.git
cd langchain-qa-astradb
``` 

2. Install the required Python packages:

```bash 
pip install -r requirements.txt
```

3. Set up your AstraDB credentials in the `.env` file:

```bash
ASTRA_DB_APPLICATION_TOKEN=AstraCS:your_application_token
ASTRA_DB_ID=your_database_id
OPENAI_API_KEY=your_openai_api_key
```

Replace the placeholders with your actual AstraDB application token, database ID, and OpenAI API key.

## Running the Application

1. Ensure your AstraDB is set up and running.
2. Run the Python script:

```bash
python app.py
```

3. The application will load the Budget_Speech.pdf, split it into chunks, and store these in AstraDB for querying.

4. You can ask questions about the content of the `Budget_Speech.pdf` document directly in the console.

## Example Usage
1. The application will prompt you to enter a question.
2. It will retrieve the most relevant text chunks from AstraDB and generate an answer using the OpenAI model.
3. The first 4 documents relevant to your question will also be displayed by relevance score.

## Files

-`app.py`: The main Python script that handles the LangChain logic, interaction with AstraDB, and Q&A functionality.
-`requirements.txt`: Lists all the Python dependencies needed to run the application.
-`.env`: Contains environment variables such as API keys and AstraDB credentials. This file should not be included in version control.
-`README.md`: This file, providing an overview of the project.
-`LICENSE`: The project's license, specifying how others may use the code.
-`.gitignore`: Specifies files and directories that should be ignored by Git, such as the .env file and any other sensitive information.
-`Budget_Speech.pdf`: The document that is used for the Q&A functionality.
-`notebook.ipynb`: A Jupyter notebook for interactive exploration and development of the Q&A system.

## License
This project is licensed under the MIT License - see the `LICENSE` file for details.

## .gitignore
The following files are ignored in the version control:
.env
__pycache__/
*.pyc
*.pyo
*.pyd

## Contributing
Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgments
Thanks to the developers of LangChain for providing powerful tools for building language model applications.
This project was inspired by the need to efficiently query large documents using natural language.

