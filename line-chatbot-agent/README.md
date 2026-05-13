# 🤖 0280 Line Chatbot Agent

## Overview
The 0280 Line Chatbot Agent workflow is designed to automate interactions with users on the Line messaging platform. With a straightforward setup, it enables seamless communication and provides quick responses based on user input, making it an essential tool for businesses looking to enhance their customer support.

## Features
- Automated conversation handling
- Configurable responses based on user queries
- Integration with Line messaging platform
- Easy to set up and maintain
- Scalable for various use cases

## How It Works
1. **Webhook Node**: Listens for incoming messages from the Line platform.
2. **Function Node**: Processes the incoming data, extracting relevant information such as user ID and message content.
3. **Switch Node**: Directs the flow based on the user's message, allowing for different responses based on keywords.
4. **Respond Node**: Sends predefined or customized replies back to the user on Line.

## Prerequisites
- A Line account
- n8n instance setup
- Webhook URL available for Line integration
- Necessary API credentials for accessing Line's messaging services

## Setup Instructions
1. Download the `0280-line-chatbot-agent.json` file.
2. Open your n8n instance.
3. Go to the Workflows section and click on "Import".
4. Upload the `0280-line-chatbot-agent.json` file.
5. Configure the Webhook node with your Line API credentials.
6. Save and activate the workflow.

## Configuration

| Variable          | Description                                |
|-------------------|--------------------------------------------|
| LINE_CHANNEL_ID   | Your Line channel ID for the messaging API|
| LINE_CHANNEL_SECRET| Your Line channel secret for authentication |
| RESPONSE_DELAY    | Time delay before sending responses (in ms) |

## Usage
To trigger the workflow, send a message to your Line account linked with the channel ID configured in the workflow. The chatbot will respond according to the programmed response logic.

## Nodes Used

| Node Type      | Purpose                            |
|----------------|-----------------------------------|
| Webhook        | Receives incoming messages        |
| Function       | Processes the incoming data       |
| Switch         | Directs flow based on user input  |
| Respond        | Sends replies back to the user    |

## Error Handling
Make sure to handle potential errors by implementing a catch node in n8n. This will log any unexpected behaviors or issues, allowing for easier debugging.

## License
MIT