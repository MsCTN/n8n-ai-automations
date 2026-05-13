# 🚀 n8n Workflow: Milvus RAG Chatbot

## Overview
This n8n workflow is designed to integrate with Milvus for building a Retrieval-Augmented Generation (RAG) chatbot. It allows you to chat with users while leveraging advanced data retrieval mechanisms to provide smarter responses. This automation streamlines the query process and enhances user interaction.

## Features
- Seamless integration with Milvus for data retrieval
- Intelligent response generation based on queried data
- Easy to customize and extend
- Comprehensive error handling included

## How It Works
1. **Start Node**: Initiates the workflow upon receiving a trigger event.
2. **Milvus Node**: Connects to the Milvus database and retrieves relevant data based on user input.
3. **Response Generation Node**: Takes the retrieved data and formulates a coherent response using Generative AI capabilities.
4. **Output Node**: Sends the generated response back to the user or the originating system.

## Prerequisites
- An active Milvus instance: Ensure you have access to a running Milvus database.
- Valid API credentials for connecting to Milvus.
- An n8n account with access permissions to create and edit workflows.

## Setup Instructions
1. Download the workflow JSON file: `0461-milvus-rag-chatbot-flow.json`.
2. Open your n8n editor.
3. Click on the "+" icon to import the workflow.
4. Select the JSON file and import it.
5. Configure the Milvus node with your API credentials.
6. Validate and save your workflow.

## Configuration

| Variable                | Description                                         |
|-------------------------|-----------------------------------------------------|
| `milvus_url`           | URL of the Milvus instance to connect to.           |
| `milvus_collection`     | The collection name in Milvus where data is stored. |
| `response_format`      | Define the format for the generated response.       |

## Usage
To trigger the workflow, send a user query through the designated input channel. The workflow will automatically process the input and return the generated response from the chatbot.

## Nodes Used

| Node Type        | Purpose                                           |
|-------------------|---------------------------------------------------|
| Start             | Initiates the workflow                            |
| Milvus            | Fetches relevant data based on user query        |
| Response Generator | Generates response using the retrieved data       |
| Output            | Outputs the final response back to the user      |

## Error Handling
The workflow includes built-in error handling mechanisms. If any node fails, an error message will be logged, and a fallback response will be generated to inform users of the issue.

## License
MIT License. See the [LICENSE](LICENSE) file for more details.