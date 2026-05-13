# 🛠️ n8n Workflow: Follow Up Meetings

## Overview
This n8n workflow is designed to automate follow-up meetings with clients or team members. It simplifies the scheduling process, ensuring that no important meetings are overlooked. With a straightforward design, this workflow provides ease of use and efficiency in managing follow-up communications.

## Features
- Automated scheduling of follow-up meetings
- Customizable templates for email notifications
- Integration with popular calendar services
- Easy to modify and extend based on specific needs

## How It Works
1. **Trigger Node**: Initiates the workflow based on a defined event (e.g., a new contact added).
2. **Email Node**: Sends a follow-up email to the participant with predefined scheduling options.
3. **Calendar Node**: Automatically adds the confirmed meeting to a specified calendar.
4. **Webhook Node**: Listens for responses from participants regarding their availability.

## Prerequisites
- n8n instance up and running
- Email account configured for sending emails
- Access to a calendar service (Google Calendar, Outlook, etc.)
- Webhook endpoint for receiving responses

## Setup Instructions
1. Download the `3288-follow_up_meetings.json` file to your local machine.
2. Open your n8n instance and navigate to the workflows section.
3. Click on "Import" and select the downloaded JSON file.
4. Configure the credentials for the email and calendar nodes as per your account details.
5. Adjust any node settings to fit your specific use case.

## Configuration

| Variable             | Description                                             |
|----------------------|---------------------------------------------------------|
| Email Template       | The content of the follow-up email that will be sent    |
| Calendar ID          | The identifier for the calendar where meetings will be added |
| Trigger Event        | The event that starts the workflow (e.g., new contact)  |
| Time Zone            | The time zone for meeting scheduling                     |

## Usage
To trigger the workflow, make sure that the specified event occurs in your n8n instance (e.g., adding a new contact). The workflow will then automatically process the follow-up steps as configured.

## Nodes Used

| Node Type          | Purpose                                               |
|--------------------|-------------------------------------------------------|
| Trigger Node       | Initiates the workflow based on a specific event     |
| Email Node         | Sends follow-up emails to participants                 |
| Calendar Node      | Adds scheduled meetings to the calendar               |
| Webhook Node       | Listens for responses about availability from participants |

## Error Handling
In case of errors, the workflow can send error notifications via email or log them for review. Ensure that proper error handling nodes are configured to manage failures effectively.

## License
MIT