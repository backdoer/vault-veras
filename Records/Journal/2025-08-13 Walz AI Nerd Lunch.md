---
created: 2025-08-13 18:35
modified: 2025-08-13 19:30
date: 2025-08-13
journal-type: reflection
tags:
  - keep-import
---

# Walz AI Nerd Lunch

Benchmarking: Langsmith
- Trajectory benchmarking
    - "LLM as a judge"
    - Having a pass or a fail is the better way to go
    - Can be very expensive and slow
    - Determine what a good margin for error is
    - Try to add as many production use cases as possible

Try to solve a real problem that isn't summarizing

100% an art

Build for tomorrow's models - trust the models more than you should

Main problems:
- halucincations (not enough context)
- not following directions (too much context)

Scrub and pre-process to stay HIIPA compliant

MCP Server: gives the server the ability to define their own LLM tools/functions

Clean tool design is CRITICAL

Biggest gotchas:
- Getting the agent to call the right tool
- Specific names of parameters and how well they are documented/typed
- Clean results before passing back to the LLM. Can result in too much context.
- Error handling. Give as descriptive of errors as possible to the LLM. Allows the LLM to self-heal.

Prompt design:
1. Keep conditional logic to a minimum to avoid confusion. Put that higher up in the orchestration layer. 
2. Pass XML or markdown when structruing prompts.

Agent memory (and you can structure these in your prompt):
- Semantic memory (facts)
- Episodic memory (experiences)
- Procedural memory (instructions)

Summarize context and then eventually you can summarize the summaries - to keep the right amount of context.

Architecture examples:
1. React Agent
2. Plan + execute (like Claude Code checklists)
3. Multi-agent supervisor (You create multiple agents with just a couple tools each, with a supervisor).
    -  Tool agents (the supervisor sees the children as tools)
4. Multi-agent network (the nodes no about each other, not just the supervisor)

They can "transfer" between each other. Give agents specialities. 

Langs:
- Langgraph
- Langchain
- Langsmith

He doesn't recommend fine-runing models because he feels like the improvements in the models themsevles will outweigh

Human in the loop interventions (a tool you can use).

Add a reflection step in the process to make sure the requirements are met.

Nodes, edges, and conditional edges. Stay away from conditional edges wherever possible - avoid decision trees and developer decisions.



