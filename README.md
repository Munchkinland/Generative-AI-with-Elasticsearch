# ElasticDocs GPT

This is a Streamlit application that utilizes the ElasticSearch database and OpenAI's ChatGPT to answer questions based on Elastic Documentation. The application supports three search methods: BM25, ELSER, and kNN + BM25 with RRF.
Setup

Before running the application, make sure to set up the required environment variables:

    OPENAI_API_KEY: Your OpenAI API key.
    OPENAI_API_BASE: The OpenAI API base URL.
    OPENAI_API_ENGINE: The OpenAI GPT engine model.
    ELASTIC_CLOUD_ID (optional): The Elastic Cloud ID if using Elasticsearch on the cloud.
    ELASTIC_URL: The Elasticsearch URL if not using the cloud.
    ELASTIC_USER: Your Elasticsearch username.
    ELASTIC_PASSWORD: Your Elasticsearch password.
    ELASTIC_PROXY: Set to "True" if using an Elastic Proxy.
    OPENAI_API_TYPE: OpenAI API type.
    OPENAI_API_VERSION: OpenAI API version.
    ELASTIC_INDEX_DOCS: The index for ElasticSearch.

Dependencies

Make sure to install the required Python packages by running:

bash

pip install streamlit openai elasticsearch elastic-apm

Running the Application

To run the application, execute the following command in your terminal:

bash

streamlit run your_script_name.py

Replace your_script_name.py with the name of the script containing the provided code.
Usage

    Enter your question in the text input.
    Choose the search method by clicking on the corresponding button (BM25, ELSER, or kNN + BM25 with RRF).
    Optionally, you can customize the system prompt, user prompt, and negative response in the "Show Prompt Override Inputs" expander.
    Check the "Show Full Prompt Sent to LLM" checkbox if you want to display the full prompt sent to the language model.
    Click on the respective search method button to get the response.

Additional Information

    The application uses Elastic APM for performance monitoring.
    The toLLM function formats prompts and utilizes ChatGPT for generating responses.
    The Elasticsearch queries are implemented for BM25, ELSER, and kNN + BM25 with RRF.
    The application supports multiple search methods to provide diverse responses.

Feel free to explore and enhance the application further based on your needs!