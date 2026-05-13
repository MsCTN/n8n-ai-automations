# 📱 n8n Workflow: Social Media Creator

## Overview
The **Social Media Creator** workflow automates the process of generating and scheduling social media posts based on user-defined templates. It integrates seamlessly with multiple platforms, allowing for efficient content dissemination and engagement tracking.

## Features
- Create and schedule posts across various social media platforms
- Utilize customizable templates for diverse content types
- Automatically fetch and update post status
- Error logging and notification for failed posts

## How It Works
1. **Start Node**: Initiates the workflow.
2. **Fetch Data Node**: Retrieves content ideas from a specified source (e.g., Google Sheets or API).
3. **Generate Post Node**: Uses templates to create a social media post based on fetched data.
4. **Social Media Post Node**: Posts the generated content to selected social media platforms.
5. **Check Status Node**: Retrieves the posting status to ensure successful publication.
6. **Log Errors Node**: Tracks any errors encountered during the posting process.

## Prerequisites
- n8n instance set up and running
- API keys for relevant social media platforms (e.g., Twitter, Facebook, LinkedIn)
- Google Sheets or other data source access (if applicable)

## Setup Instructions
1. Download the `0007-social-media-creator.json` workflow file.
2. Open your n8n instance and navigate to the **Import** section.
3. Upload the JSON file and click on **Import**.
4. Configure the necessary credentials for social media accounts and any data sources.
5. Save and activate your workflow.

## Configuration

| Variable              | Description                                 |
|-----------------------|---------------------------------------------|
| `social_media_api_key`| API key for each social media platform     |
| `content_template`    | Template used for creating social media content |
| `data_source`         | Source for fetching content ideas           |

## Usage
To trigger the workflow, you can set it to run on a schedule or manually initiate it through the n8n dashboard. Ensure that all required credentials are properly configured before triggering.

## Nodes Used

| Node Type               | Purpose                                 |
|-------------------------|-----------------------------------------|
| Start                   | Initiates the workflow                  |
| HTTP Request            | Fetches data from external sources      |
| Function                | Generates the post content              |
| Social Media Post Node  | Posts content to social media platforms  |
| Webhook                 | Allows manual triggering of the workflow |
| Error Handling          | Manages and logs errors                 |

## Error Handling
The workflow includes an error handling mechanism that logs any failed attempts to post content. All errors are tracked, and notifications can be set to alert users of issues in real-time.

## License
MIT