# PDF-based FAQ Chatbot

This project is designed to create a custom FAQ chatbot that can answer questions based on the content of uploaded PDF documents. The chatbot leverages advanced natural language processing (NLP) techniques to extract relevant information from the PDFs and provides accurate responses to user queries.

## Features

- **PDF Content Extraction**: Upload one or multiple PDF files, and the application will extract text from them.
- **Text Chunking**: The extracted text is split into manageable chunks to facilitate efficient information retrieval.
- **Vector Store Creation**: Text chunks are embedded and stored in a vector database for quick similarity searches.
- **Conversational AI**: The chatbot uses Google Generative AI (Gemini)/custom huggingface llm to generate detailed answers based on the context provided by the PDF content.
- **User Interaction**: A simple user interface built with Streamlit allows users to ask questions and receive answers directly within the application.

## How It Works

1. **PDF Upload**: Users can upload PDF files via the sidebar.
2. **Text Processing**: The text is extracted from the PDFs, split into chunks, and stored in a vector database.
3. **Question-Answering**: Users can input a question, and the system will search for relevant information in the vector database. The chatbot then generates a detailed answer based on the context retrieved.

## Technologies Used

- **Streamlit**: Used to create the user interface.
- **PyPDF2**: For extracting text from PDF files.
- **LangChain**: Facilitates the creation of conversational AI models and processing chains.
- **Chroma**: A vector store for storing and retrieving text embeddings.
- **Hugging Face**: Provides the embeddings used for the text chunks as wall as to use custom llms.
- **Google Generative AI (Gemini)**: The model used to generate conversational responses.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AddagallaSaiTharun/FAQ_Chatbot.git
   ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Set up environment variables:
    * Create a .env file in the root directory.
    * Add your API keys and any other necessary environment variables, e.g.
    ```bash
    HF_TOKEN=<your_huggingface_token>
    GOOGLE_API_KEY=<your_GOOGLE_API>
    ```
4. Run the Streamlit application:
    ```bash
    streamlit run app.py
    ```

## Usage

* Launch the application by running the command above.

* Upload PDF files using the file uploader in the sidebar.
* Wait for the processing to complete.
* Ask any question related to the content of the PDFs, and the chatbot will provide an answer based on the information available.


## Model Customization
* Model Customization: You can switch out the default language model for another, such as Hugging Face models or other generative AI models.
* UI Customization: Modify the Streamlit interface to fit your specific needs, such as adding more features or customizing the layout.