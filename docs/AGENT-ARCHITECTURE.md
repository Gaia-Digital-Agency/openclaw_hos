# Agent Architecture

Hutton is a multi-agent AI system built on OpenClaw.

## Agents

| Agent | ID | Workspace |
|-------|----|-----------|
| **Hutton** | main | workspace-main |
| **Booking** | booking | workspace-booking |
| **Sales** | sales | workspace-sales |
| **FNB** | fnb | workspace-fnb |
| **Event** | event | workspace-event |
| **Maintenance** | maintenance | workspace-maintenance |
| **Housekeeping** | housekeeping | workspace-housekeeping |
| **Concierge** | concierge | workspace-concierge |
| **Front** | front | workspace-front |
| **Writer** | writer | workspace-writer |

## Delegation

Hutton (main) delegates to: booking, sales, fnb, event, maintenance, housekeeping, concierge, front, writer

## Configuration

- State dir: `/opt/.openclaw-hos`
- Config: `/opt/.openclaw-hos/openclaw.json`
- Gateway port: 18989
- Model: deepseek/deepseek-chat (fallback: google/gemini-2.5-flash)

## Workspace Structure

Each agent workspace follows:

```
workspace-{agent}/
  IDENTITY.md      -- Name, role
  SOUL.md          -- Voice and output rules
  USER.md          -- Owner context
  TOOLS.md         -- Available tools
  SKILLS.md        -- Skill index
  SKILL-*.md       -- Specific workflows
```
