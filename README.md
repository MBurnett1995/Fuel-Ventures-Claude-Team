# Fuel Ventures — Claude Team OS

This repository is the source of truth for how Fuel Ventures uses Claude Team. It contains the system prompts, skill definitions, output templates, and connector setup guides that power our AI stack.

---

## What This Repo Is

We run Claude Team as a centralised intelligence layer across the firm — connecting it to Google Drive, Pipedrive, Visible.vc, Notion, Linear, Gmail, and Slack via MCP. Each department has a dedicated Project (agent) pre-configured with the right data sources and context.

This repo version-controls all of that configuration. When a system prompt is improved, a new skill is proven in practice, or a template is updated, it gets committed here — so we have a full history of what changed, why, and what worked.

---

## Structure

```
Fuel-Ventures-Claude-Team/
│
├── projects/          # System prompts for each department Project
│   ├── bd/
│   ├── portfolio/
│   ├── lp-comms/
│   ├── compliance/
│   └── operations/
│
├── skills/            # Slash command definitions — added once workflows are proven
│   ├── bd/
│   ├── portfolio/
│   ├── lp-comms/
│   └── operations/
│
├── templates/         # Output templates Claude references for consistent formatting
│   ├── ic-memo.md
│   ├── board-prep.md
│   └── lp-update.md
│
└── mcp/               # Step-by-step connector setup guides
    ├── google-drive.md
    ├── pipedrive.md
    ├── visible-vc.md
    └── notion.md
```

---

## Department Projects

| Project | Who it's for | Connected to |
|---|---|---|
| BD | Partners, Associates | Pipedrive, Google Drive, Gmail |
| Portfolio | Portfolio team, Partners | Visible.vc, Google Drive, Pipedrive |
| LP & Comms | Partners, Comms lead | Google Drive, Gmail, Notion |
| Compliance | Operations, Finance, Partners | Google Drive |
| Operations | Admin, Ops team | Gmail, Slack, Linear, Notion, Google Drive |

---

## How This Repo Gets Updated

**Projects** are updated when a system prompt is materially improved — not for every minor tweak. If you change a Project's prompt and the output quality improves noticeably, commit it with a note on what changed and why.

**Skills** are only added once a workflow has been run and optimised in practice. If you're writing the same prompt three or more times and it consistently produces good output, it's ready to become a skill. Document it here before adding it to Claude Team.

**Templates** are updated when the output format changes — e.g. if the IC memo structure is revised, the template here should reflect it so Claude's outputs stay consistent.

---

## Getting Set Up

New to the team? Start here:

1. Accept your Claude Team invite (check your @fuel.ventures inbox)
2. Sign in at [claude.ai](https://claude.ai) with your Fuel Ventures Google account
3. Find the shared Projects in the left sidebar
4. Follow the connector setup guides in `/mcp/` to link your accounts
5. Read the system prompt for your department's Project so you understand what it's configured to do

For questions, speak to Michael.

---

## Stack

| Tool | Role |
|---|---|
| Claude Team | Primary AI interface |
| Google Drive (Fuel Vault) | Document repository |
| Pipedrive | CRM and deal pipeline |
| Visible.vc | Portfolio KPIs and reporting |
| Notion | Internal knowledge base |
| Linear | Task and project tracking |
| Gmail | Founder, LP, co-investor comms |
| Slack | Internal comms |
