🧭 3. Info Tracker CLI
Purpose

Acts as a developer/operator-facing command-line interface for managing and visualizing the evolution of information over time.

Responsibilities

Query relationships and evolution trees between information nodes.

Perform manual linking or unlinking of related information.

Display clusters, statistics, and confidence scores.

Trigger re-indexing or rescoring jobs.

Review low-confidence matches queued for human verification.

Core Components

CLI Framework: Built using Cobra (Go CLI framework).

Query Engine: Calls tracker service API or directly queries the DB.

Visualization Module: ASCII or graphical tree view of relations.

Review Manager: Human-in-the-loop validation of linked data.

Example Commands
pits-cli view --info-id=1234
pits-cli cluster --date=2025-01-01
pits-cli review --pending
Output

Interactive CLI feedback and optionally JSON export for automation.