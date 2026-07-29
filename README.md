# n8n AI Automations

A curated collection of production-focused n8n workflows for AI agents,
CRM automation, RAG, lead generation, email processing, customer support,
recruitment, voice agents and business operations.

## What This Repository Contains

This repository demonstrates practical automation architectures using n8n,
REST APIs, webhooks, databases, vector stores and leading AI models.

Each featured workflow includes:

- Business use case
- Architecture overview
- Required integrations
- Setup instructions
- Workflow JSON export
- Example input and output
- Security considerations
- Error-handling notes

## Featured Workflows

| Workflow | Business Use Case | Main Technologies |
|---|---|---|
| Adaptive RAG Strategy | Selects an appropriate retrieval strategy for user queries | n8n, Gemini, vector search |
| CRM Lead Automation | Classifies enquiries and creates CRM records | n8n, CRM API, OpenAI |
| WooCommerce Support Agent | Automates product and order enquiries | WooCommerce, AI agent |
| Voice RAG Assistant | Answers knowledge-base questions through voice | ElevenLabs, RAG, n8n |
| AI CV Screening | Evaluates and categorizes candidates | AI, document processing |
| Social Media Factory | Generates and distributes content | AI models, social APIs |
| Email Phishing Analysis | Analyzes suspicious email content | Email, AI classification |
| Calendar AI Agent | Manages calendar-related requests | Google Calendar, AI |
| Bidirectional Sync | Synchronizes records between platforms | APIs, data mapping |
| n8n Workflow Backup | Automates workflow backups | n8n API, storage |

## Workflow Categories

### AI Agents and RAG

- Adaptive RAG Strategy
- AI Chat with Supabase Documents
- Voice RAG Assistant
- PDF-to-Vector-Store Automation

### CRM and Sales

- CRM Lead Automation
- ERP Lead Automation
- Customer Lead Processing
- HubSpot ChatGPT Integration

### Email Automation

- Email AI Assistant
- Gmail Auto Responder
- Email Phishing Analysis
- Email Summary Agent

### Recruitment and HR

- AI CV Screening
- AI Interview Flow
- Candidate Assessment
- HR CV Evaluation

### Content and Marketing

- Automated Social Media Factory
- LinkedIn AI Post
- Automated Blog Creation
- SEO Audit Report

## Importing a Workflow

1. Download the required workflow JSON file.
2. Open your n8n instance.
3. Select **Import from File**.
4. Upload the JSON file.
5. Configure the required credentials.
6. Replace example IDs, URLs and variables.
7. Test the workflow using non-production data.
8. Activate it only after reviewing every node.

## Security Notice

The workflows do not intentionally include usable credentials.

Before running any workflow:

- Review every credential reference
- Replace example webhook URLs
- Confirm data-retention requirements
- Test using non-sensitive records
- Apply least-privilege permissions
- Add error handling and execution monitoring

Never commit API keys, passwords or client data.

## Compatibility

Workflows may require different n8n versions, nodes or external services.
Check the individual workflow documentation before importing.

## Disclaimer

These workflows are provided as implementation references. Production
deployment requires testing, credential configuration, security review,
rate-limit handling and environment-specific adjustments.

## Maintainer

Muhammad Siddique  
Full-Stack Developer and AI/CRM Automation Specialist

Website: https://theperfectsol.com  
GitHub: https://github.com/MsCTN
