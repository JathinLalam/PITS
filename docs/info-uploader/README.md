☁️ 4. Info Uploader
Purpose

Uploads processed and structured data into the final destination systems (e.g., ArangoDB, vector stores, or knowledge graph databases) for indexing, visualization, and analytics.

Responsibilities

Push data from processed store to the graph or vector database.

Manage batch uploads and retries.

Maintain synchronization state (uploaded / pending / failed).

Support incremental updates and deletions.

Optionally publish events (Kafka/HTTP) for downstream consumers.

Core Components

Uploader Engine: Handles concurrency and retries.

State Tracker: Maintains upload progress.

Adapter Layer: Abstract interface to support multiple destinations (e.g., ArangoDB, Qdrant, Elasticsearch).

Output

Fully loaded information nodes and relationships in production DB.

pits-uploader --target=arangodb --batch-size=1000 --resume