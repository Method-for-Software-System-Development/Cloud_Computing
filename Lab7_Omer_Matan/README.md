# Microservices Search & Rating System

This project demonstrates a lightweight **Microservices architecture** for managing, indexing, and searching documents, with support for logical operators (AND / OR) and a basic rating mechanism.

## Architecture Overview

The system is modular and built around four independent services:

- **DocumentService** – responsible for storing and retrieving documents
- **IndexService** – builds and queries an inverted word index
- **RatingService** – allows users to rate documents and calculates average scores
- **ResultFormatter** – formats search results with metadata and ratings

Each service encapsulates its own state and logic, enabling scalable and testable design.

## Services Documentation

### DocumentService

- `add_document(title, content)` → Adds a new document and returns its metadata
- `get_document(doc_id)` → Retrieves a document by its ID

### IndexService

- `index_document(doc_id, content)` → Indexes a document’s content
- `search(terms, mode='AND')` → Searches for documents containing all (`AND`) or any (`OR`) of the terms

### RatingService

- `add_rating(doc_id, score)` → Submits a rating (1–5) for a document
- `get_avg_rating(doc_id)` → Returns the average rating (or None if no ratings)

### ResultFormatter

- `format_results(doc_ids, doc_service, rating_service)` → Returns structured info including title, snippet, and score

## Usage Example

```python
# 1. Add documents
doc_service.add_document("Intro to AI", "Artificial intelligence is the future of technology.")
doc_service.add_document("Cloud", "Cloud computing enables scalable architectures.")

# 2. Index them
index_service.index_document("1", "Artificial intelligence is the future of technology.")
index_service.index_document("2", "Cloud computing enables scalable architectures.")

# 3. Add ratings
rating_service.add_rating("1", 5)
rating_service.add_rating("2", 3)

# 4. Search using AND
results = index_service.search(["cloud", "ai"], mode="AND")
formatted = format_results(results, doc_service, rating_service)

# 5. Search using OR
results = index_service.search(["cloud", "ai"], mode="OR")
formatted = format_results(results, doc_service, rating_service)
```

## Test Results

| Scenario | Input | Output |
|---------|--------|--------|
| `AND` search for `['cloud', 'ai']` | No common document | `[]` |
| `OR` search for `['cloud', 'ai']` | Docs 1 and 2 found | Average scores: 5.0 and 3.0 |
| Add rating of 4 to Doc 1 | Score updated | New average: 4.5 |
| Retrieve document by ID | `"1"` | Title and 100-char snippet displayed |
