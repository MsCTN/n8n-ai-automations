# 📹 TikTok to YouTube Generator Workflow

This n8n workflow automates the process of converting TikTok videos into YouTube-ready content. By leveraging various integrations, this workflow significantly streamlines content creation and distribution across both platforms.

## Features
- Seamless integration between TikTok and YouTube.
- Automation of video downloads and uploads.
- Customizable video captions and tags.
- Error handling to manage potential issues during processing.

## How It Works
1. **Start Node**: Initiates the workflow based on triggers or schedules.
2. **TikTok Node**: Fetches a specific TikTok video using its URL or ID.
3. **Formatting Node**: Processes the video for compatibility with YouTube (resolution, aspect ratio adjustments).
4. **YouTube Node**: Uploads the processed video to the specified YouTube channel.
5. **Notification Node**: Sends a confirmation message once the upload is complete.

## Prerequisites
- An active TikTok account with access to the videos you want to use.
- A YouTube channel where you plan to upload videos.
- n8n instance properly set up and running.
- Required API credentials for TikTok and YouTube.

## Setup Instructions
1. Download and import the workflow JSON file (`2937-tiktok-youtube-generator.json`) into your n8n instance.
2. Configure the TikTok node with your credentials and the video link.
3. Adjust any settings in the Formatting and YouTube nodes to meet your specific requirements.
4. Set up credentials for the Notification node if logging or notification is enabled.

## Configuration

| Variable            | Description                                           |
|---------------------|-------------------------------------------------------|
| `tiktokVideoUrl`    | The URL of the TikTok video to be processed          |
| `youtubeChannelId`  | The ID of your YouTube channel for uploads            |
| `videoTitle`        | Title for the uploaded video on YouTube              |
| `videoDescription`  | Description accompanying the YouTube video            |
| `videoTags`         | Tags to include for better discoverability on YouTube |

## Usage
To trigger the workflow, set it to run on a schedule or initiate it manually within the n8n interface.

## Nodes Used

| Node Type       | Purpose                                                |
|------------------|-------------------------------------------------------|
| TikTok Node      | Fetches video data from TikTok                        |
| Formatting Node   | Prepares video for upload to YouTube                 |
| YouTube Node     | Uploads the processed video to the specified channel   |
| Notification Node | Sends notification upon successful upload             |

## Error Handling
The workflow includes error handling nodes that capture any issues during the processing stages. Failed uploads will trigger alerts that can be logged or reported via email/SMS.

## License
MIT