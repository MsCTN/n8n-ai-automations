# 📹 YouTube Video Analysis Workflow

This n8n workflow automates the analysis of YouTube videos to extract valuable insights. By leveraging various integrations, it allows users to gather, process, and analyze video data efficiently.

## Features
- Extract video metadata from YouTube.
- Analyze video engagement metrics.
- Store results in a structured format for further analysis.
- Support for integration with third-party applications (e.g., Google Sheets, Slack).

## How It Works
1. **YouTube Node**: Fetches the video details based on the provided video ID.
2. **Function Node**: Processes the fetched data to calculate metrics such as view count, likes, and comments.
3. **Google Sheets Node**: Stores the processed data in a Google Sheets document for easy access.
4. **Slack Node**: Sends a summary notification to a specified Slack channel regarding the analysis.

## Prerequisites
- An active YouTube API key.
- A Google account with access to Google Sheets.
- A Slack workspace with a valid webhook URL for notifications.

## Setup Instructions
1. Import the JSON file into n8n using the "Import" feature.
2. Configure the required credentials for YouTube, Google Sheets, and Slack.
3. Update the video ID in the YouTube node configuration.

## Configuration

| Variable          | Description                                            |
|-------------------|--------------------------------------------------------|
| `video_id`        | The ID of the YouTube video to analyze.               |
| `slack_webhook`   | The webhook URL for sending notifications to Slack.    |
| `google_sheet_id` | The ID of the Google Sheet where results will be stored.|

## Usage
Trigger the workflow manually in n8n or set it to run on a schedule to analyze new videos regularly.

## Nodes Used

| Node Type        | Purpose                                                     |
|-------------------|-------------------------------------------------------------|
| YouTube           | Fetches video information                                   |
| Function          | Processes the video data and calculates metrics            |
| Google Sheets     | Stores the results for easy access and analysis            |
| Slack             | Notifies about the analysis results in a Slack channel     |

## Error Handling
- The workflow includes error triggers that log issues if fetching data fails, allowing for prompt troubleshooting.
- Notifications are sent via Slack if any node encounters an error during execution.

## License
MIT