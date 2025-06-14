# AI-Agents-and-Workflows

This repository contains a collection of AI agents and automation workflows built with n8n, designed to streamline various tasks and processes.

📂 Contents
**Chatbot.json**
An n8n workflow that exposes a webhook chat trigger and routes messages through a LangChain “AI Agent” (using a memory buffer window) to answer FAQ-style queries for an accounting firm. 

**Drive_RAG_chatbot.json**
An n8n pipeline that watches a Google Drive folder, downloads documents, splits them, creates embeddings via OpenAI, and inserts them into an in-memory vector store to enable Retrieval-Augmented Generation. 

**Hosted_RAG_chatbot.json**
Similar to Easy RAG but using Pinecone as a hosted vector store: it downloads files, extracts text, generates embeddings with OpenAI, and upserts to a Pinecone index for RAG. 

**Auto_Email.json**
An n8n workflow for automated email QA: it extracts PDF/Word attachments, filters them, runs a self-assessment prompt through OpenAI, and replies to the sender via Gmail. 

**chatbot.html**
A standalone HTML/CSS/JS snippet to embed the n8n chat widget on a web page, with custom theming and configuration pointing at your n8n webhook. 

**Auto_form.json**
An n8n form-triggered workflow: on submission it filters by budget, branches via a Switch node, sends tailored Gmail responses, notifies internal teams, and logs entries into Google Sheets.

**Email_automation.json**
An n8n workflow that reads incoming IMAP emails, uses a LangChain extraction agent and a Code node to parse quote request details into JSON, generates a formal proposal email via OpenAI, sends a draft internally for approval with the Send & Wait for Response node, and upon approval dispatches the finalized offer to the client.
