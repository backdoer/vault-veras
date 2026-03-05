---
created: 2025-08-29 13:13
modified: 2025-09-19 21:13
date: 2025-09-19
journal-type: reflection
tags:
  -


# Database Architecture

Todos:
✅ Replace denormalized fields with kysely across time schema
✅ Remove denormalized fields
❌ Use kysely for archivals (blocked by schema gen)
✅ Try prisma join mode

Final thoughts:
- 2 db schemas and prisma client each what are you
   - LOVE prisma’s type generation and simplicity
   - Prisma relations are not efficient at scale 
   - automatically prevents bad prisma nesting 
   - timeseries extension on time client
   - allow different patterns for the time data
   - auto-generated kysely client 
   - prisma auto-generated “where” types 
       - mapper from prisma to kysely where
       - stays shallow with no nested relations
- Time partitioning on the time schema 
   - keep partition count small (non-time queries)
   - archive old data into s3 parquet
       - kysely (ts) to enrich, query by partition name
- Normalize
   - join 1:1 data with kysely and stitch 1:many data
   - denormalize ids (like a star schema)
   - get rid of unnecessary sync functions 
   - remove unnecessary denormalized fields
- No cross-schema foreign keys
   - prisma won’t allow it, unfortunately 

Questions:
- Prisma join vs query mode 
    - query mode (default) ALWAYS stitches
    - join mode (new) ALWAYS does lateral joins 
         - I like that this preserves node cpu/memory
         - In this mode, can do 1-offs in query mode 

Nice-to-haves:
✅ When an include gets passed in, have the returned type reflect that it's there

Fields to normalize:
- Facility
   - Employer
- Agency
- Shift position
- Shift template
- User
- Employee
- Areas (stitch)


Longterm: 
- Hot/cold separation of data?
- Single tenant
- Quarterly partitions with higher retention if needed
   - Could partition by facility and have different retention lengths for diff partitions
