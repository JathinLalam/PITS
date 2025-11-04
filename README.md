# PITS

Public Information Tracking System (PITS)

This document describes the architecture and individual service responsibilities for the Public Information Tracking System (PITS). The project is designed in Go and currently divided into four core services:

Info Collector

Info Converter

Info Tracker CLI

Info Uploader

Each service is modular and can be extended with additional APIs, agents, or MCP (Model Context Protocol) integrations.

## 🧩 Inter-Service Workflow

Info Collector → Gathers raw data → stores in /data/raw.

Info Converter → Transforms raw → structured information units.

Info Uploader → Uploads structured data to graph/vector DB.

Info Tracker CLI → Used by developers/operators to explore, validate, and manage evolution of data.

🔧 Tech Stack
Component	Technology	Purpose
Core Language	Go	High performance, concurrency, and modularity
Database	PostgreSQL / ArangoDB	Relational & Graph storage
Vector Store	Qdrant / Weaviate	Semantic similarity and embeddings
Message Broker	Kafka / NATS	Event streaming between services
CLI Framework	Cobra	Developer CLI commands
Scheduler	Cron / Go routines	Timed or triggered collection
Containerization	Docker + Compose	Deployment & scaling
📈 Future Extensions

MCP integration for AI agents.

LLM-based summarization and topic classification.

Web dashboard for visualization.

Source reliability and confidence scoring.

Author: PITS Core Team

Built with ❤️ in Go — scalable, modular, and future-ready.