---
created: 2025-11-12 20:16
modified: 2025-11-12 20:35
date: 2025-11-12
journal-type: reflection
tags:
  -


# Start Putting Tenant Ids on All Tables

Start putting tenant ids on all tables

The application is the best place to put it but it's the hardest place to put it. The application can do it better than operations.

It's a question of where you want to put the pain and suffering and put the work

If you're able to pull the data out and put it into a cache layer that isn't dependent on the database, you will be in a much better place. Takes away that centralized dependency. Only centralize the settings IF you can do this.

Be careful with too much replication

Try to get rid of all joins against the user table - the centralized table. If we try to replicate that data to all shards, we WILL have a replication issue.

With multi tenant, someone will suffer.


