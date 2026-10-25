---
description: "Write a handoff document for a fresh agent to continue work"
---

Write a handoff document summarising the current conversation so a fresh agent can continue the work. Save to the temporary directory of the user's OS ($TMPDIR, else /tmp; %TEMP% on Windows) - not the current workspace.

Include a "Suggested skills" section in the document, naming which skills the next agent should call the Skill tool for.

Do not duplicate content already captured in other artifacts (specs, plans, ADRs, issues, commits, diffs). Reference them by path or URL instead.

Redact any sensitive information, such as API keys, passwords, or personally identifiable information.

Focus: $ARGUMENTS

If $ARGUMENTS is provided, treat it as a description of what the next session will focus on and tailor the doc accordingly. If empty, summarise the full conversation.
