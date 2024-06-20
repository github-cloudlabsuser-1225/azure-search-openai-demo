# Backend Documentation

This document provides an overview and setup instructions for the backend component of the Azure Search OpenAI Demo application.

## Overview

The backend of the Azure Search OpenAI Demo is built using [Quart](https://quart.palletsprojects.com/), a Python framework for asynchronous web applications. It is responsible for handling requests from the frontend, processing them with Azure AI and OpenAI services, and returning the results.

## Getting Started

### Prerequisites

- Python 3.7 or higher
- Pipenv or any Python virtual environment manager
- Azure subscription (for Azure AI services)

### Setup

1. Clone the repository to your local machine.

    ```shell
    git clone https://github.com/Azure-Samples/azure-search-openai-demo.git
    ```

2. Navigate to the `app/backend` directory.

    ```shell
    cd azure-search-openai-demo/app/backend
    ```

3. Install the required Python packages.

    ```shell
    pipenv install
    ```

    Or using pip:

    ```shell
    pip install -r requirements.txt
    ```

4. Set up environment variables. Create a `.env` file in the `app/backend` directory and add the necessary Azure and OpenAI credentials:

    ```plaintext
    OPENAI_API_KEY=<Your OpenAI API Key>
    AZURE_SEARCH_API_KEY=<Your Azure Search API Key>
    AZURE_SEARCH_SERVICE_NAME=<Your Azure Search Service Name>
    AZURE_SEARCH_INDEX_NAME=<Your Azure Search Index Name>
    ```

5. Start the backend server.

    ```shell
    pipenv run python app.py
    ```

    Or using Python directly:

    ```shell
    python app.py
    ```

    The server will start running on `http://127.0.0.1:5000`.

## Features

- **AI Chat HTTP Protocol**: The backend adheres to the [AI Chat HTTP Protocol](https://aka.ms/chatprotocol), facilitating communication between the frontend and backend.
- **Integration with Azure AI and OpenAI**: Processes requests using Azure Cognitive Search for document retrieval and OpenAI's GPT models for generating responses.
- **Asynchronous Request Handling**: Built with Quart for efficient handling of concurrent requests.

## Customization

Refer to the [Customizing the Backend](../../../../c:/Users/azureuser/azure-search-openai-demo/docs/customization.md#customizing-the-backend) section in the customization guide for details on how to customize the backend for your needs.

## Contributing

We welcome contributions and suggestions. Please refer to the [Contributing Guidelines](../../../../c:/Users/azureuser/azure-search-openai-demo/CONTRIBUTING.md) for more information.

## License

This project is licensed under the MIT License - see the [LICENSE](../../../../c:/Users/azureuser/azure-search-openai-demo/LICENSE) file for details.