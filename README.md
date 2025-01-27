## Features
- Entity and Relationship Extraction: The system uses natural language processing (NLP) to extract named entities and identify relationships between them in multilingual text.
- Interactive chatbot: The chatbot is capable of answering user questions using information extracted from documents and pre-processed data.
- LangChain Integration: An application integrates with the LangChain library, making it easy to build natural language processing pipelines and implement language models.
- Multilingual support: The system is designed to handle data in different languages, allowing for broader interaction with users from diverse backgrounds.

## Objective

The goal of this project is to demonstrate how advanced NLP techniques can be applied to create more intelligent and responsive chatbots. The application can be used in a variety of contexts, including customer service, technical support, and education systems, where fast and accurate responses are essential. Feel free to adjust any text as needed to fit the style of your project or include additional information that you consider relevant! If you need further assistance, I'm here to help.

## Configuration

Create a .env file in the root directory and add the following environment variables:
```
OPENAI_API_KEY=<YOUR_OPENAI_API_KEY>

NEO4J_URI=<YOUR_NEO4J_URI>
NEO4J_USERNAME=<YOUR_NEO4J_USERNAME>
NEO4J_PASSWORD=<YOUR_NEO4J_PASSWORD>

HOSPITALS_CSV_PATH=https://raw.githubusercontent.com/hfhoffman1144/langchain_neo4j_rag_app/main/data /hospitals.csv
PAYERS_CSV_PATH=https://raw.githubusercontent.com/hfhoffman1144/langchain_neo4j_rag_app/main/data/payers.csv
PHYSICIANS_CSV_PATH=https://raw.githubusercontent.com/hfhoffman1144/langchain_neo4j_rag_app/main/data/physicians.csv PATIENTS_CSV_P ATH=https://raw.githubusercontent.com/hfhoffman1144/langchain_neo4j_rag_app/main/data/patients.csv
VISITS_CSV_PATH=https://raw.githubusercontent.com/hfhoffman1144/langchain_neo4j_rag_app/main/data/visits.csv
REVIEWS_CSV_PATH=https://raw.githubusercontent. com/hfhoffman1144/langchain_neo4j_rag_app/main/data/reviews.csv

HOSPITAL_AGENT_MODEL=gpt-3.5-turbo-1106
HOSPITAL_CYPHER_MODEL=gpt-3.5-turbo-1106
HOSPITAL_QA_MODEL=gpt-3.5-turbo-0125

CHATBOT_URL=http://host.docker.internal:8000/hospital-rag-agent
```

The chatbot uses OpenAI LLMs, so you will need to create an OpenAI API key and store it as OPENAI_API_KEY.

The three NEO4J_ variables are used to connect to your Neo4j AuraDB instance. Follow the instructions here to create a free instance.

Once you have a Neo4j instance running and filled in all the environment variables in .env, you can run the entire project with Docker Compose. You can install Docker Compose by following these instructions.

Once you have filled in all the environment variables, configured a Neo4j AuraDB instance, and installed Docker Compose, open a terminal and run:

```
$ docker-compose up --build
```

After each container has finished building, you will be able to access the chatbot API at http://localhost:8000/docs and the Streamlit application at http://localhost:8501/.
