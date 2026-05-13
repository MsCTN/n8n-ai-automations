# 📦 n8n Workflow: Onfleet Shopify Task

## Overview
This n8n workflow integrates Onfleet and Shopify, allowing you to automate tasks related to order management and delivery. With this workflow, you can streamline your operations and enhance the efficiency of your business processes.

## Features
- Automated task creation in Onfleet for new Shopify orders.
- Real-time updates between Shopify and Onfleet.
- Customizable node settings to fit your business needs.

## How It Works
1. **Webhook Node**: Listens for new Shopify orders.
2. **Shopify Node**: Retrieves order details and customer information from Shopify.
3. **Onfleet Node**: Creates a new delivery task in Onfleet using the order details.
4. **Set Node**: Prepares additional information for logging or further processing.
5. **HTTP Request Node**: Updates Shopify with the task status or any relevant information from Onfleet.

## Prerequisites
- n8n instance set up and running.
- Valid API credentials for Onfleet and Shopify.
- Access to Onfleet and Shopify accounts.

## Setup Instructions
1. Download the JSON file: [0140-onfleet-shopify-task.json](path-to-your-file).
2. Open n8n and go to the workflow editor.
3. Click on the “Import” button and upload the JSON file.
4. Configure your credentials for Onfleet and Shopify in the nodes.

## Configuration

| Variable              | Description                                        |
|-----------------------|----------------------------------------------------|
| `WEBHOOK_URL`         | The URL to receive the webhook from Shopify.       |
| `SHOPIFY_API_KEY`     | Your Shopify API Key for authentication.           |
| `ONFLEET_API_KEY`     | Your Onfleet API Key for delivery task creation.   |

## Usage
To trigger the workflow, simply ensure your Shopify store is configured to send webhooks on new orders to the specified `WEBHOOK_URL`.

## Nodes Used

| Node Type          | Purpose                                     |
|---------------------|---------------------------------------------|
| Webhook             | Receives incoming requests from Shopify.    |
| Shopify             | Fetches order details from Shopify.         |
| Onfleet            | Creates a delivery task in Onfleet.         |
| Set                 | Prepares data for further processing.        |
| HTTP Request        | Sends status updates back to Shopify.       |

## Error Handling
Errors are logged within n8n. It is recommended to set up additional error handling nodes to manage outcomes like failed API requests or missing order details.

## License
MIT