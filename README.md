STAT3 LINT


                                                              
STAT3 LINT is a Cognitive State Linting Protocol designed for AI coding agents. It enforces structured thinking, prevents infinite execution loops, and mitigates context bloat by utilizing markdown memory files to meticulously track the agent's cognitive state.

The Problem
AI agents often suffer from:

Execution Loops: Repeating the same failed attempts or getting stuck in circular reasoning.
Context Bloat: Accumulating unnecessary context, leading to forgotten instructions, hallucination, and degraded performance.
Loss of State: Forgetting the current objective or failing to logically progress through complex, multi-step tasks.
The Solution: STAT3 LINT
STAT3 LINT introduces a lightweight, text-based protocol that enforces discipline on the agent's internal state management. By treating the agent's working memory as a lintable artifact, we can ensure consistent, goal-oriented behavior.

Core Rules
Single Active State: The agent must operate within exactly one well-defined cognitive state at any given time (e.g., PLANNING, EXECUTING, DEBUGGING, VERIFYING).
Strict State Progression: Transitions between states must follow a logical, predefined flow. Arbitrary jumping between disjointed tasks is prohibited.
Blocker Resolution Contract: When blocked, the agent must formally declare the blocker, document the attempted resolutions, and define the criteria for unblocking before proceeding or escalating.
Working Memory Pruning (Max 10 Items): To prevent context bloat, the agent's active working memory is strictly limited to 10 items. Older or irrelevant items must be summarized and archived or discarded.
Evidence-Based Completion: A task or state cannot be marked as complete without explicitly referencing the empirical evidence that validates the completion.
Usage
STAT3 LINT is implemented via system prompt injection. See the 
System Prompts
 directory for copy-paste templates to integrate STAT3 LINT into your agent's context.
