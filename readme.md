# AI Chatbot Agent with LangGraph, Groq, and Tavily Search

This project showcases the development of an AI chatbot agent that leverages the capabilities of LangGraph, Groq's language models, and Tavily for enhanced web search functionality. The application features a FastAPI backend and a Streamlit frontend, allowing users to interact with the AI agent through a user-friendly web interface.

## Key Features

*   **Multiple Language Model Support:** Integrates with Groq's language models, specifically `llama-3.3-70b-versatile` and `mixtral-8x7b-32768`. The architecture is designed to be extensible to support other models and providers, such as OpenAI.
*   **Web Search Integration:** Uses Tavily to enable the agent to perform web searches, thereby providing responses based on up-to-date information.
*   **Customizable Agent Behavior:** Users can define a custom system prompt to shape the agent's personality and behavior.
*   **Streamlit UI:** Offers an intuitive and interactive web interface using Streamlit for a seamless user experience.
*   **FastAPI Backend:** Employs FastAPI to handle API requests and orchestrate the agent's logic efficiently.
*   **Pydantic Validation:** Uses Pydantic for input data validation, ensuring data integrity and reliability.
* **Dynamic model selection**: User can select the AI model in the frontend.
* **Multiple Provider Support**: User can select the model provider in the frontend.

## Project Structure

*   `.env`: Stores sensitive information like API keys for Groq and Tavily. It should be kept private and not committed to version control.
*   `.gitignore`: Specifies files and directories that Git should ignore, such as the `.env` file, virtual environments (`.venv/`), and Python cache directories (`__pycache__/`).
*   `ai_agent.py`: Contains the core logic for interacting with the AI agent. This includes setting up the LLM, tools, and the LangGraph agent with its state modifier.
*   `backend.py`: Implements the FastAPI application, defines the API endpoint for the chatbot, and handles requests by sending them to the `ai_agent.py` file.
*   `frontend.py`: Contains the Streamlit application code, responsible for creating the user interface and sending requests to the backend.

## Technologies Used

*   **LangGraph:** Used to create the conversational agent that can maintain state and interact with tools.
*   **Groq:** Provides high-performance language models (`llama-3.3-70b-versatile`, `mixtral-8x7b-32768`).
*   **Tavily:** Enables the agent to perform web searches.
*   **FastAPI:** A modern, high-performance web framework for building APIs.
*   **Streamlit:** Used for creating the interactive web-based user interface.
*   **Pydantic:** Provides data validation and parsing capabilities for API requests.
*   **Python:** The primary programming language used for the project.
*   **Dotenv**: For managing environment variables.

## Setup and Installation

1.  **Clone the Repository:**

   
    git clone https://github.com/Dataworld123/Basic_Chatbot_Agent.git

2.  **Environment Variables:**

    *   Create a `.env` file in the root directory of the project.
    *   Add your Groq and Tavily API keys to the `.env` file:

        ```properties
        GROQ_API_KEY='your_groq_api_key'
        TAVILY_API_KEY='your_tavily_api_key'
        ```
    **Important**: Replace `'your_groq_api_key'` and `'your_tavily_api_key'` with your real api keys.
    * The value must not have extra space.

3.  **Install Dependencies:**

    It is recommended to use a virtual environment. If you are using conda:
    
    conda create -p 
    .venv\Scripts\activate  # On Windows

   Requirements:
    pip install langchain-groq langchain-community fastapi uvicorn python-dotenv pydantic requests streamlit tavily-python
    ```

4.  **Run the Backend:**

    ```bash
    python backend.py
    ```

    This will start the FastAPI server, typically at `http://127.0.0.1:8688`.

5.  **Run the Frontend:**

    Open a new terminal, activate the virtual environment and then:
    ```bash
    streamlit run frontend.py
    ```

    This will launch the Streamlit application in your web browser (usually at `http://localhost:8501`).

## Usage

1.  **Access the Web Interface:** Open your web browser and go to `http://localhost:8501`.
2.  **Define Agent:** In the "Define your AI Agent" text area, enter a system prompt to customize the AI agent's behavior and personality.
3. **Select a model and provider:** Select the AI Model and the provider.
4.  **Enable Web Search:** If you want the agent to use Tavily for web search, check the "Allow Web Search" checkbox.
5.  **Enter Query:** In the "Enter your query" text area, type your question or request.
6.  **Ask Agent:** Click the "Ask Agent!" button to send your query to the AI agent.
7.  **View Response:** The agent's response will be displayed below.

## Future Enhancements

*   **More LLMs:** Add support for more language models and providers, such as more models from OpenAI.
*   **Conversation History:** Implement conversation history to create a more interactive experience.
* **Error handling**: improve error handling in the frontend and backend.
* **Design**: improve design.


##  NOTE :  Run frontend and Backend in different terminal , first run backend then run frontend.