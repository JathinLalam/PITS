### 🛰️ 1. Info Collector
Purpose

Responsible for ingesting information from external public-domain sources (e.g., GDELT) and storing it in a raw data format for further processing.

Responsibilities

Fetch data periodically or on-demand from GDELT API.

Maintain local cache for fetched datasets.

Store raw data into a staging database (Postgres/ArangoDB).

Log metadata (timestamp, source URL, batch ID).

Retry failed downloads and maintain data integrity.

## Core Components

Collector Engine: Goroutines for parallel data fetching.

Scheduler: Cron or Kafka-based trigger to fetch periodically.

Validation Layer: Verifies file integrity and schema before saving.

## Output

Raw, unprocessed event data in JSON/CSV format stored in /data/raw or database table raw_information.

Example CLI Usage

pits-collector --source=gdelt --since=2024-01-01 --until=2024-12-31