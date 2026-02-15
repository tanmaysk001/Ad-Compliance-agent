# Azure Multi-modal Compliance Ingestion Engine using LangGraph

## Description

This project is an intelligent video compliance ingestion and analysis system built on Azure cloud services and orchestrated using LangGraph. The system automatically processes video content from YouTube, extracts multi-modal insights (OCR, transcription, visual analysis), and performs compliance auditing using AI-powered analysis.

The solution combines Azure Video Indexer for content extraction, Azure AI Search for semantic retrieval, and Azure OpenAI for intelligent analysis through a RAG (Retrieval-Augmented Generation) workflow. It provides both a FastAPI backend for programmatic access and a CLI interface for batch processing.

Key capabilities include:
- Automated video download and processing
- Multi-modal content extraction (text, audio, visual)
- Semantic search across video content
- AI-powered compliance auditing
- Full observability with Azure Application Insights and Langsmith tracing

## Architecture

![Project Architecture](Project2_Langgraph_Architecture.png)

The architecture consists of:

- **Entry Points**: CLI trigger (main.py) and FastAPI server backend
- **Orchestration**: LangGraph RAG workflow, video processor, retrieval engine, and compliance auditor
- **Azure Infrastructure**: Blob Storage for temporary files, Video Indexer for OCR/transcription, and AI Search vector database
- **External Services**: YouTube video source, Azure OpenAI for LLM and embeddings, Application Insights for monitoring, and Langsmith for tracing
