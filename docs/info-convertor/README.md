🔁 2. Info Converter
Purpose

Processes raw data collected by the Info Collector and converts it into normalized, structured entities suitable for graph or relational storage.

Responsibilities

Parse raw GDELT data (CSV/JSON) into typed Go structs.

Extract entities: actors, locations, organizations, event types.

Compute embeddings (semantic similarity) and enrich with metadata.

Detect duplicates or updates to existing records.

Generate output schema for storage or further analysis.

Core Components

Parser: Converts raw GDELT fields into Go models.

Enricher: Adds NLP embeddings, location normalization, and tags.

Transformer: Converts to internal InformationUnit struct.

Validator: Ensures required fields exist.

Output

Structured data saved in processed_information table or /data/processed directory.

Example CLI Usage

pits-converter --input=/data/raw --output=/data/processed