# Architecture Plans

## Service Architecture

- Remix continues as the BFF layer indefinitely
- Backend services can be extracted as needed for isolation or language flexibility
- Extracted services can share the same single-tenant databases, pooled through PgBouncer

## Node Performance

- Abstract worker threads to offload CPU-intensive tasks off the main thread
- Use Node Clinic for profiling and identifying bottlenecks

## Database Strategy

### Core
- Cache the majority of reads in Redis

### Reporting
- Migrate to a dedicated Postgres instance
- Scale reads with replicas
- Implement time partitioning

### Integrations
- Evaluate moving to DynamoDB for better write scaling
- Implement more aggressive data retention / cleanup cycles

### Tenant Isolation
- Distribute load across multiple databases
- Offer single-tenant databases for large customers
- Apply time partitioning for historical data
- Option: custom web URL per shard for full single-tenant deployments
