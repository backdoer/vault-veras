---
created: 2024-03-20 03:48
modified: 2024-03-22 05:08
date: 2024-03-22
journal-type: reflection
tags:
  - keep-import
---

# Azure SSO Instructions

Enterprise Application:
- Create a Jobwise application from non-gallery configuration

App Registration:
- Overview
   - Give me your tenant ID
- Manifest
   - Add roles, logo url, and home page URL

Enterprise Application:
Provisioning:
- Tenant URL: https://provisioning.jobwise.com/scim/azure/v1/93c1680b-e1a5-4495-a6ba-9d1d4ea523b0
- Send error emails to tyler@jobwise.com
- Add roles mapping
   - Expression
   - SingleAppRoleAssignment([appRoleAssignments])
   - roles[primary eq "True"].value
- Add your users and groups and assign them roles
- Run "Provisioning on Demand" to test it out


Unnecessary:
- Authentication
   - Add a web platform
        - Redirect URsI: 
             - https://sso.jobwise.com/auth/azure/redirect
             - https://jobwise.com/auth/azure/redirect
