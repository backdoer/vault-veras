---
created: 2025-07-15 19:16
modified: 2025-07-15 19:44
date: 2025-07-15
plan-type: checklist
tags:
  -


# Rory and Tyler

They recommend timescale cloud
Check if timescale cloud supports terraform
Add compliance to the checklist
Could use garden for local development
- doesn't have to run in a remote environment, can work locally
- would this work for Wildfire?
- can deploy 3rd party helm charts
- Can work as a full-fledged orchestration tool for all environments
- Minimal differences is best case scenario
Need to figure out env (use AWS secret manager or github secrets)
Set up cost alerts early

Keep the code and the terraform separate

They recommend kuberenetes as our orchestration layer
Using garden locally would force us to learn kuberenetes

AWS' hosted prometheus is rediculously overpriced
