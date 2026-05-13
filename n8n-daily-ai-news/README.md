# 📄 n8n Daily AI News Workflow

## Overview
The **Daily AI News** workflow automates the retrieval and aggregation of the latest news articles related to artificial intelligence. Leveraging n8n's powerful automation capabilities, this workflow enables users to stay updated effortlessly with the most relevant news articles delivered regularly.

## Features
- Automatic fetching of daily AI-related news articles
- Integration with popular news APIs
- Customizable output format
- Easy setup and configuration
- Error handling and notifications

## How It Works
1. **Start Node**: Triggers the workflow either on a defined schedule or manually.
2. **HTTP Request Node**: Sends a request to the news API to fetch the latest articles related to AI.
3. **JSON Parse Node**: Processes the response from the API to extract relevant information.
4. **Filter Node**: Filters articles based on predefined criteria (e.g., publication date, relevance).
5. **Set Node**: Formats the news articles into a user-friendly structure.
6. **Send Email Node**: Sends an email containing the curated articles to the specified recipients.
7. **End Node**: Marks the completion of the workflow.

## Prerequisites
- n8n running locally or on a cloud provider
- API key for the news service (e.g., NewsAPI)
- Email service account for sending notifications

## Setup Instructions
1. Download the workflow JSON file: [0544-n8n-daily-ai-news.json](./0544-n8n-daily-ai-news.json).
2. Open n8n and navigate to the workflow section.
3. Import the JSON file using the import feature.
4. Configure the HTTP Request Node with your news API credentials.
5. Set up the Send Email Node with your email service details.

## Configuration

| Variable          | Description                                  |
|-------------------|----------------------------------------------|
| `api_key`         | Your API key for accessing the news service.|
| `recipient_email` | The email address to receive news updates.  |
| `schedule_time`   | The time of day to trigger the daily news. |

## Usage
To trigger the workflow, you can either run it manually from the n8n interface or set it to execute on a specified schedule. Make sure that the nodes are configured correctly with the necessary credentials.

## Nodes Used

| Node Type        | Purpose                                       |
|------------------|-----------------------------------------------|
| Start Node       | Initiates the workflow based on schedule/manual trigger. |
| HTTP Request Node| Fetches news articles from the external API. |
| JSON Parse Node  | Parses the API response to extract information. |
| Filter Node      | Filters articles based on defined criteria.   |
| Set Node         | Structures the articles for output.           |
| Send Email Node  | Sends the final curated news to recipients.   |

## Error Handling
The workflow includes error handling mechanisms that notify you via email if any node fails. Ensure to check logs for specific errors to troubleshoot effectively.

## License
MIT