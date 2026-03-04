---
created: 2022-05-26 00:01
modified: 2022-05-27 16:43
date: 2022-05-27
journal-type: reflection
tags:
  - keep-import
---

# Turborepo vs NX

Turborepo vs NX
Next vs. Remix
Vercel vs. Netlify vs. AWS vs. fly.io 

Typescript
FE tests



Things to try:
- Authentication
- Connect to Postgres
- Directory structure & organization (DDD)
- CI/CD deployment pipeline (Github Actions)
- Build simple CRUD table
- Background processing
- QA pre-deploy
- Logs (logdna or datadog)
- Performance (datadog)
- Tests
- Error handling
- Exception monitoring
- Websockets and real-time 
- Import and Export 



Options:
- Phoenix on fly.io w/ postgres on fly
   - real-time: phoenix channels and/or liveview
   - pub-sub: oban 
   - cron: quantum or oban 
- Next on vercel with planetscale
   - real-time: pusher or ably 
   - pub-sub: lambdas with sqs 
   - cron: vercel cron 
- Remix on fly.io with postgres 
   - real-time: node web sockets 
   - pub-sub: node job scheduler (Bree)
   - cron: node cron (Bree) 















