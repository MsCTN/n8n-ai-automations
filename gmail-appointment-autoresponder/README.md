# 📧 Gmail Appointment Autoresponder Workflow

## Overview
This n8n workflow automatically responds to Gmail messages regarding appointment inquiries. It streamlines communication by sending prompt replies, ensuring no potential client goes unanswered. This workflow enhances productivity by reducing the time spent on manual email responses.

## Features
- Automatically replies to Gmail appointment requests.
- Customizable email templates.
- Supports multiple appointment types.
- Easy to import and configure.

## How It Works
1. **Gmail Trigger Node**
   - Activates the workflow when a new email is received in the Gmail account.

2. **Filter Node**
   - Checks if the email subject contains specific keywords related to appointment requests.

3. **Set Node**
   - Prepares the response email using a template that includes the sender's name and appointment details.

4. **Gmail Send Node**
   - Sends the autoresponse email to the original sender of the inquiry.

## Prerequisites
- A Gmail account with IMAP enabled.
- n8n installation (self-hosted or cloud).
- Necessary n8n credentials for your Gmail account.

## Setup Instructions
1. Download the workflow JSON file: `0279-gmail-appointment-autoresponder.json`.
2. Open your n8n editor.
3. Click on "Import" and upload the JSON file.
4. Configure the Gmail credentials by setting up your Google API credentials and enabling the required scopes.

## Configuration

| Variable           | Description                                           |
|--------------------|-------------------------------------------------------|
| `GMAIL_USER`       | The email address from which the autoresponder will send emails. |
| `KEYWORDS`         | A list of keywords or phrases that indicate an appointment request. |
| `RESPONSE_TEMPLATE`| The template for the autoresponse email.             |

## Usage
The workflow triggers automatically when a new relevant email is received in your Gmail account. Ensure that the specified keywords in the filter node match the incoming emails.

## Nodes Used

| Node Type          | Purpose                                             |
|--------------------|----------------------------------------------------|
| Gmail Trigger      | Listens for new emails in your Gmail inbox.       |
| Filter             | Checks if the email subject meets certain criteria.|
| Set                | Prepares an autoresponse email based on a template.|
| Gmail Send         | Sends the prepared autoresponse email to the sender.|

## Error Handling
In case of any errors during execution, the workflow is set up to log the error for troubleshooting. You can review the execution log in your n8n instance to take necessary actions.

## License
MIT