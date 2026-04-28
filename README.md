# Life OS Agent

A personal decision engine that manages human attention and task prioritization.

## What it is
Not a reminder app. Not a chatbot. Not a full AI.

It is a decision engine that asks:
- What should I interrupt this person with?
- When should I interrupt them?
- Should I interrupt them at all?
- When should I stop asking?

## What it does
1. Reads a list of tasks (medication, prayer, habits, deadlines)
2. Scores each task by urgency, importance, and prior attempts
3. Decides: ASK / WAIT / SUPPRESS / BATCH
4. Logs every decision to the console
5. Repeats every 30 seconds

## Current status
SHADOW MODE - no notifications, no UI, no database.
Console logs only. Observing decision quality.

## Tech stack
- Node.js
- tasks.json for task storage
- Plain .js files, no frameworks

## File structure
life-os/
├── tasks.json      ← task data
├── scorer.js       ← priority scoring
├── decision.js     ← ASK/WAIT/SUPPRESS/BATCH logic
├── loop.js         ← main loop, runs every 30 seconds
└── logger.js       ← console + file logging

## Task types
- medication (high priority, time sensitive)
- prayer (high priority, time windows)
- habits (medium priority, daily)
- tasks (variable priority, deadline based)

## Decision types
- ASK: interrupt the user now
- WAIT: not yet, check again later
- SUPPRESS: too many attempts, back off
- BATCH: combine with other pending items

## Priority rules
Score increases with:
- urgency (closer deadline)
- importance of task type

Score decreases with:
- repeated ignoring
- multiple prior attempts

## Attention constraints
- Limited interruptions per hour
- Max retries per task
- Quiet mode when limits exceeded

## Next steps
1. Build tasks.json with real tasks
2. Build scorer.js
3. Build decision.js
4. Build loop.js
5. Build logger.js
6. Run and observe output

## How to continue this project
Share this GitHub link with Claude or Claude Code at the start of every session.
Say: "Read the README and continue building Life OS Agent."
