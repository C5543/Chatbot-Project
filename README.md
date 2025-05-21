# RAG Chatbot Project 🤖

A full-stack Retrieval-Augmented Generation (RAG) chatbot built with FastAPI, Streamlit, and ChromaDB, and deployed on Microsoft Azure using Terraform and CI/CD pipelines via GitHub Actions.

📌 Project Overview
This project aims to explore three deployment architectures on Azure for a production-ready AI chatbot:

Server-based Deployment

Serverless Deployment

Containerized Deployment

The chatbot integrates retrieval-based search with generative AI, enabling users to ask questions about uploaded PDF documents with accurate and context-rich answers.

🎯 Objectives
Develop and test the chatbot locally.

Deploy the application on Azure using:

Virtual Machines (VM/VMSS)

Azure Functions (Serverless)

Azure Container Apps (Containerized)

Automate infrastructure provisioning using Terraform.

Build CI/CD pipelines using GitHub Actions.

🏗️ Project Stages & Milestones
🔹 Local Development (Stage 1–4)
Build a basic Streamlit chatbot.

Separate frontend (Streamlit) and backend (FastAPI).

Connect to a database and implement chat history.

Add RAG functionality using PDF documents.

🔹 Milestone 1: Server-based Deployment (Stage 5–6.6)
Manually deploy app on Azure VMs.

Add Azure PostgreSQL, Blob Storage, and Key Vault.

Transition to Terraform-based infrastructure.

Set up CI/CD pipelines for automatic VM deployment.

Finalize staging and production environments using VMSS and App Gateway.

🔹 Milestone 2: Serverless Deployment (Stage 7–9)
Migrate backend from FastAPI to Azure Functions.

Store chat history in CosmosDB.

Use Azure Function Bindings to process files.

Automate deployment via GitHub Actions.

🔹 Milestone 3: Containerized Deployment (Stage 10)
Dockerize FastAPI backend.

<img src="https://github.com/user-attachments/assets/7df8ed06-ded5-4e84-bf0f-e9d3d31f0905" width="400" />


Deploy to Azure Container Apps.

Store container images in Azure Container Registry.

Finalize with CI/CD pipeline for automatic container updates.

🛠️ Tech Stack
Layer	Technology
Frontend	Streamlit
Backend	FastAPI
Vector DB	ChromaDB
File Storage	Azure Blob Storage
Metadata DB	Azure PostgreSQL
History DB	Azure Cosmos DB
Secrets Mgmt	Azure Key Vault
DevOps	Terraform, GitHub Actions
Deployment	VM / Azure Function / ACA

📦 Repository Structure
```  graphql

Chatbot-Project/
├── backend/             # FastAPI code
├── frontend/            # Streamlit app
├── terraform/           # Terraform modules and configs
├── workflows/           # GitHub Actions CI/CD
├── pdfs/                # Sample PDFs for testing
├── requirements.txt     
└── README.md
```

🚀 How to Run Locally

``` bash
# Clone the repository
git clone https://github.com/C5543/Chatbot-Project.git
cd Chatbot-Project

# Install dependencies
pip install -r requirements.txt

# Start backend
cd backend
uvicorn main:app --reload

# Start frontend
cd ../frontend
streamlit run app.py
```
🔐 Environment Variables
``` makefile
POSTGRES_URL=
CHROMADB_PATH=
AZURE_STORAGE_KEY=
AZURE_COSMOS_KEY=
OPENAI_API_KEY=
```
🎓 Acknowledgments
This project was developed as part of my journey with the Saudi Digital Academy, powered by WeCloudData.

<img src="https://github.com/user-attachments/assets/41ac8274-c361-4c2c-8fc8-7746c00b5823" width="400" />

