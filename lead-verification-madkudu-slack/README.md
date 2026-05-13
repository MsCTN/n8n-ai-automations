# 📊 n8n Workflow: Lead Verification with MadKudu and Slack

## Overview
This n8n workflow automates the process of lead verification by integrating MadKudu's lead scoring capabilities with Slack notifications. It streamlines the workflow by notifying your team of lead statuses in real time, ensuring timely follow-ups.

## Features
- Real-time lead scoring through MadKudu
- Notifications sent to Slack channels
- Customizable lead verification criteria
- Easy to import and configure
- Error handling for failed API calls

## How It Works
1. **Trigger Node:** Initiates the workflow when a new lead is received.
2. **MadKudu Node:** Sends the lead information to MadKudu for scoring.
3. **Conditional Node:** Checks the lead score and decides the next steps.
4. **Slack Node:** Sends notifications regarding lead status based on the outcome of the conditional check.

## Prerequisites
- MadKudu API access
- Slack account with a workspace to send notifications
- n8n instance set up and running

## Setup Instructions
1. Download the workflow JSON file `0342-lead-verification-madkudu-slack.json`.
2. Open your n8n instance.
3. Navigate to the "Workflows" tab and click on "Import."
4. Select the downloaded JSON file and import it.
5. Configure the necessary credentials (MadKudu API key, Slack webhook) in the n8n credentials manager.

## Configuration

| Variable         | Description                                   |
|------------------|-----------------------------------------------|
| `madkudu_api_key`| Your MadKudu API key for accessing the service|
| `slack_webhook`  | The Slack incoming webhook URL for notifications|

## Usage
Trigger the workflow by adding a new lead to your integrated application. The workflow will automatically execute and provide lead verification results.

## Nodes Used

| Node Type     | Purpose                                      |
|---------------|----------------------------------------------|
| Trigger       | Start the workflow upon new lead creation   |
| MadKudu       | Obtain the lead score from MadKudu          |
| Conditional    | Evaluate the lead score for further action   |
| Slack         | Notify the team of lead verification status  |

## Error Handling
In case of failed API calls, the workflow includes error handling nodes that log the error and notify a specified Slack channel to alert the team of issues.

## License
MIT