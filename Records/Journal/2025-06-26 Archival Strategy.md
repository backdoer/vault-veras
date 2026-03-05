---
created: 2025-06-25 14:30
modified: 2025-06-26 04:22
date: 2025-06-26
journal-type: reflection
tags:
  -


# Archival Strategy


- add runDelete flag
- double check time span logic
- allow 5 years for messaging 
- Use explicit zod to define the archival schema
- Type safety against the prisma type to make sure the schemas align
- Convert the zod schema to a parquet schema
- Automated schema versioning in a postgres table when changes happen
- Partition by table, version, employer, facility, month, year,
    - Need to normalize the timescale chunking into month/year
- Archive chunks in a separate cron after confirmation that data is present
- Store json as a string 
- Formatter fn to take in table type and return parquet schema 
- Audit trail of archive jobs 
