---
created: 2025-06-19 17:44
modified: 2025-06-19 19:12
date: 2025-06-19
journal-type: reflection
tags:
  - keep-import
---

# Reasoning for Timescale and Denormalization

Pros:
Timeseries queries/reporting
Database portability
Read speed (no joins & chunked access for range queries)
Data archival
Historical immutability
Limited to ~84 chunks due to constraints/archival

Cons:
Storage
Data duplication/staleness
Id updates have to span chunks (though only 84 chunks)
Relational integrity
Querying not by range:
- Overlapping range queries
- By user id only, etc.
