# 📦 n8n Workflow: Telegram AI Assistant

## Overview
The Telegram AI Assistant workflow enables seamless interaction with users via Telegram, utilizing AI capabilities to respond to queries and manage conversations intelligently. This automation enhances user experience, allowing for quick and effective communication without manual intervention.

## Features
- AI-driven chat responses
- Integration with Telegram for messaging
- Configurable parameters for tailored interactions
- Real-time message processing
- Scalable for various use cases

## How It Works
1. **Telegram Trigger Node**: This node listens for incoming messages from a specified Telegram bot.
2. **Function Node (Process Message)**: Extracts the text from the incoming message and prepares it for AI processing.
3. **AI Service Node**: Sends the processed message to an AI service for generating a response.
4. **Function Node (Prepare Response)**: Formats the response from the AI to ensure it’s suitable for Telegram.
5. **Telegram Send Message Node**: Sends the AI-generated response back to the user in the Telegram chat.

## Prerequisites
- Telegram account and bot created via BotFather
- n8n installed and running
- AI service API key (e.g., OpenAI, Dialogflow)

## Setup Instructions
1. Download the workflow JSON file `0842-telegram-ai-assistant.json`.
2. Open your n8n instance in a web browser.
3. Go to the 'Workflows' section and click 'Import'.
4. Upload the `0842-telegram-ai-assistant.json` file.
5. Configure the Telegram Trigger Node with your bot token.
6. Set up the AI service node with the necessary API key and configurations.

## Configuration

| Variable            | Description                                          |
|---------------------|------------------------------------------------------|
| `telegramBotToken`  | The authentication token for your Telegram bot.     |
| `aiServiceApiKey`   | The API key for the AI service you are using.       |

## Usage
Trigger the workflow by sending a message to the configured Telegram bot. The bot will process your input and respond with an AI-generated answer.

## Nodes Used

| Node Type                | Purpose                                               |
|--------------------------|-------------------------------------------------------|
| Telegram Trigger         | Listens for incoming messages from Telegram bot.      |
| Function (Process Message)| Extracts and preprocesses the incoming message text.  |
| AI Service               | Generates a response using AI based on the input.     |
| Function (Prepare Response)| Formats the AI response for sending via Telegram.    |
| Telegram Send Message    | Sends the AI response back to Telegram chat.          |

## Error Handling
The workflow should handle errors gracefully by logging them and sending an error message back to the user if the AI service fails to respond or the message processing encounters an issue.

## License
MIT