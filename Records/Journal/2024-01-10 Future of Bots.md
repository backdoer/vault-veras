---
created: 2024-01-10 00:39
modified: 2024-01-10 02:54
date: 2024-01-10
journal-type: reflection
tags:
  - keep-import
---

# Future of Bots

Bot per phone number? 
- we'd need different phone numbers for job seekers and employers

Bot per conversation?
- We'd need a conversation resource for admin bots

We don't really need to worry about making sure introductions are made anymore

Some intents that just always respond regardless of the state of the bot? Because if a bot turns off or gets passed by a different bot, its intents don't mean anything anymore.
- PREF
- SHIFT
- etc.

A more GPT-enabled, open bot?

The ability to have micro intents? And a conversation is waiting for one specific type of message?
- Specify what you want to listen for when you send a message

Don't use bots for everything so that intents don't get in each other's way?

Bot responsibilities currently include:
- intent matching
- guarding
- templating

Should we pull templating out?

The sendOutboundUserTextMessage worker currently handles:
- throttling
- preventing late texts
- rate limits

What's the right relationship with notifications?
