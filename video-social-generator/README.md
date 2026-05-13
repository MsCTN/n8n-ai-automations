# 🎬 Video Social Generator Workflow

## Overview
The Video Social Generator workflow for n8n automates the process of generating social media content from video files. It streamlines the conversion, editing, and sharing of video clips on various social platforms, enhancing productivity and creativity.

## Features
- Converts video files for social media use
- Automatically edits video segments
- Supports multiple social media platforms
- Customizable post parameters
- Easy integration with other n8n workflows

## How It Works
1. **Start Node**: The workflow begins with a trigger node that listens for new video files added to a specified location.
2. **Video Processing Node**: This node takes the input video and processes it to generate suitable segments for social media.
3. **Editing Node**: Automatically applies editing filters or transitions to enhance the clips.
4. **Export Node**: Outputs the edited clips in the desired format and resolution.
5. **Social Media Post Node**: Publishes the videos to selected social media accounts, including descriptions and hashtags.
6. **Confirmation Node**: Sends a confirmation message once the files are successfully posted.

## Prerequisites
- n8n instance running and accessible
- Social media accounts with API access (e.g., Facebook, Twitter, Instagram)
- Appropriate credentials for uploading and posting content

## Setup Instructions
1. Download the workflow JSON file: [1416-video-social-generator.json](./1416-video-social-generator.json).
2. Open your n8n instance.
3. Go to the workflows section and click on "Import".
4. Choose the downloaded JSON file to import the workflow.
5. Configure the nodes with your specific account credentials and settings.

## Configuration

| Variable          | Description                              |
|-------------------|------------------------------------------|
| videoPath         | Path to the input video file             |
| outputPath        | Destination for the edited video clips   |
| socialAccounts     | List of social media accounts to post to |
| postDescription   | Default description for social media posts |
| postHashtags      | Default hashtags to include with posts    |

## Usage
To trigger the workflow, simply upload a video file to the designated input folder linked with the Start Node. The automation will process the video and post it to your configured social accounts.

## Nodes Used

| Node Type           | Purpose                        |
|---------------------|--------------------------------|
| Start Node          | Trigger workflow on file upload |
| Video Processing Node| Process the uploaded video     |
| Editing Node        | Apply custom edits to the video|
| Export Node         | Save the edited video clips    |
| Social Media Post Node| Publish videos to social accounts |
| Confirmation Node   | Send notifications of success  |

## Error Handling
In case of errors, the workflow includes error function nodes to handle failures such as file processing issues or posting failures. Notifications can be configured to alert users regarding such errors.

## License
**MIT License**. See the [LICENSE](./LICENSE) file for more information.