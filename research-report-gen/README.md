# 🚀 n8n Workflow: Research Report Generator

## Overview
The Research Report Generator workflow automates the process of compiling research reports using various data sources. This powerful workflow efficiently processes and formats your research data, saving time and ensuring consistency in your reports.

## Features
- Automatically collects data from multiple sources.
- Generates formatted research reports based on predefined templates.
- Supports customizable configurations for data input and output.
- Easy integration with various n8n nodes for enhanced functionality.

## How It Works
1. **Node 1: HTTP Request Node**
   - Fetch data from a specified API endpoint or external source.
  
2. **Node 2: Function Node**
   - Process the incoming data to extract relevant information needed for the report.

3. **Node 3: Template Node**
   - Generate a report using a template that incorporates the processed data.

4. **Node 4: Email Node**
   - Send the generated report via email to specified recipients.

## Prerequisites
- n8n instance set up and running.
- Access to relevant data sources (e.g., APIs).
- Email account for sending reports.

## Setup Instructions
1. Download the workflow JSON file: [0976-research-report-gen.json](0976-research-report-gen.json).
2. Open your n8n instance.
3. Navigate to the "Workflows" section and click on "Import."
4. Upload the downloaded JSON file to import the workflow.
5. Configure the nodes with your required credentials and settings.

## Configuration

| Variable            | Description                                      |
|---------------------|--------------------------------------------------|
| `apiEndpoint`       | The URL of the data source to fetch research data. |
| `emailRecipient`    | The email address to send the report to.        |
| `templateId`        | Identifier for the report template to use.      |

## Usage
To trigger the workflow, simply execute it within the n8n interface or set up a webhook that triggers the workflow on demand.

## Nodes Used

| Node Type       | Purpose                                               |
|------------------|-----------------------------------------------------|
| HTTP Request     | Fetches research data from APIs or external sources.|
| Function         | Processes and formats the data for the report.     |
| Template         | Generates the report based on the processed data.  |
| Email            | Sends the final report to specified recipients.     |

## Error Handling
In case of any errors during execution, the workflow will gracefully handle exceptions by logging error details. Review the execution logs to troubleshoot any issues.

## License
This project is licensed under the MIT License.