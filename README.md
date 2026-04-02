# AI Chatbot to Guide User Workflow

A GSoC 2026 project for Jenkins — an AI-powered chatbot that helps users navigate Jenkins workflows, access documentation, and troubleshoot issues using natural language.

## About

This plugin integrates an AI chatbot directly into Jenkins UI, allowing users to ask questions and get answers grounded in official Jenkins documentation — without leaving Jenkins.

## Current Progress

- RAG pipeline using FAISS + sentence-transformers
- Local LLM: Mistral 7B via llama-cpp (no cloud dependency)
- FastAPI backend with session management
- Answers questions from Jenkins official docs

## Tech Stack

- Python, FastAPI, LangChain
- FAISS (vector search)
- Mistral 7B Q4_K_M (local LLM via llama-cpp)
- sentence-transformers/all-MiniLM-L6-v2

## What I Changed from Original Plugin

- Downloaded Mistral 7B Q4_K_M GGUF model from HuggingFace
- Rebuilt FAISS index using Jenkins documentation chunks
- Fixed metadata format to match plugin expected schema
- Resolved dependency conflicts (langchain, python-multipart)
- Verified end-to-end: question → RAG retrieval → LLM answer

## Example Output

Question: How to create a Jenkins pipeline?
Answer: To create a Jenkins pipeline, follow these steps:
1. Install Jenkins and the Pipeline plugin
2. Create a new Jenkins project
3. Create a Jenkinsfile in your repository
4. Write pipeline stages using Pipeline syntax
5. Commit the Jenkinsfile to source control

## GSoC 2026

- Proposal: AI Chatbot to Guide User Workflow
- Organization: Jenkins
- Contributor: Mimi-pan
- Mentors: Kris Stern, Shivay Lamba, Chirag Gupta
