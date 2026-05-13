# 🚀 Automated Social Media Factory Workflow

## Overview
The Automated Social Media Factory is designed to streamline and automate your social media posting process. This n8n workflow allows users to schedule and publish posts across multiple platforms, ensuring a consistent online presence with minimal manual effort.

## Features
- Multi-platform support for seamless social media management
- Customizable scheduling for posts
- Easy integration with various content sources
- Flexible media handling for images, videos, and links

## How It Works
1. **Trigger Node**: Initiates the workflow based on a set schedule or event.
2. **Content Retrieval Node**: Collects content from a specified source, such as a Google Sheet or an RSS feed.
3. **Media Processing Node**: Prepares and formats images or videos for posting.
4. **Social Media Node**: Publishes the content to selected social media platforms (e.g., Twitter, Facebook).
5. **Notification Node**: Sends a confirmation message or report about the post status to specified recipients.

## Prerequisites
- Active accounts on social media platforms (e.g., Twitter, Facebook)
- API keys or authentication tokens for each social media account
- Access to a content management source (e.g., Google Sheets, RSS feeds)

## Setup Instructions
1. Download the workflow JSON file: `1409-automated_social_media_factory.json`.
2. Open n8n and navigate to the "Import" section.
3. Upload the JSON file to n8n.
4. Configure all nodes with your account credentials and customize settings as needed.
5. Save and activate the workflow.

## Configuration

| Variable               | Description                                      |
|-----------------------|--------------------------------------------------|
| `SocialMediaAPIKey`   | API key for accessing social media accounts      |
| `ContentSourceURL`    | URL for retrieving content from the source       |
| `PostSchedule`        | Schedule for when to publish the posts           |

## Usage
To trigger the workflow, you can either use the manual trigger feature in n8n or set it to automatically execute based on the defined schedule or event.

## Nodes Used

| Node Type          | Purpose                                      |
|-------------------|----------------------------------------------|
| Trigger           | Starts the workflow based on time or event  |
| HTTP Request      | Fetches content from external sources        |
| Set               | Configures and sets variables for next nodes |
| Social Media Post  | Publishes content to selected platforms      |
| Send Email        | Notifies users about the posting status      |

## Error Handling
In case of any errors during execution, the workflow is designed to log errors and send notifications to specified recipients. Ensure proper configurations to handle failures effectively.

## License
MIT