# AWS Bedrock RAG Chatbot with S3 Knowledge Base

This project implements an Enterprise-grade RAG (Retrieval-Augmented Generation) pipeline using Amazon Bedrock Managed Knowledge Bases and Amazon S3. The AI assistant is capable of retrieving accurate, context-specific information directly from internal company documents.

## 🏗️ Architecture & Workflow
1. **Data Storage (Amazon S3):** Company policy documents, operation manuals, and guidelines are securely stored in an S3 bucket.
2. **Knowledge Base (Amazon Bedrock):** S3 is connected to Bedrock’s Managed Knowledge Base, which automatically syncs, chunks, and indexes the documents into a managed vector store using the Titan Embeddings model.
3. **Retrieval & Generation:** The system uses advanced AI models (e.g., Anthropic Claude) to answer queries grounded exclusively on the uploaded internal data, complete with reference citations.



## 🚀 Features
- Secure cloud-based internal documentation retrieval.
- Grounded responses with precise source references.
- Scalable, serverless infrastructure managed entirely by AWS.

## 📄 Included Files
- `Company_Policy_Manual.txt`: Sample operations and remote work policy manual used as the knowledge source.

## 🛠️ Setup & Deployment Steps
1. **Create S3 Bucket:** Set up an S3 bucket and upload your organization’s `.txt` or `.pdf` files.
2. **Configure Bedrock Knowledge Base:** - Go to Amazon Bedrock -> Knowledge Bases -> Create Managed KB.
   - Attach your S3 bucket as the data source.
   - Select the `Titan Embeddings G1 - Text` model for vector conversion.
3. **Test via Playground:** Use the built-in testing console in Bedrock to query the knowledge base with models like Claude Sonnet/Haiku.
