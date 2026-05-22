# Fuel Ventures — Claude Team

Configuration repository for Fuel Ventures' Claude Team workspace.

## Context

Fuel Ventures uses Claude Team as the firm-wide AI workspace, rolled out across ~20 people. It sits alongside our core stack and reads from / writes to it via connectors.

Claude Team is used for drafting, synthesis, research, reporting, and day-to-day knowledge work across investment, BD, operations, IR, compliance, and comms.

## Integrations

**Essential (Week 1)**
- **Google Drive** — canonical knowledge base
- **Slack** — primary internal comms
- **Linear** — task and project management
- **Google Sheets** — fund model, trackers, cap tables (via Drive)

**Investment & portfolio**
- **Visible.vc** — LP reporting, portfolio company KPIs, fund metrics
- **Pipedrive** — deal flow, BD pipeline, investor pipeline

**Comms & enrichment**
- **Gmail** — email drafting, thread summarisation
- **Clay** — expert network, LinkedIn enrichment, prospect research
- **Notion** — under review; Drive is canonical

Each integration has a named owner, defined scope (read vs. read-write), and is tracked in the Integrations Register (`/mcp/README.md`). Connectors come online in phases — essentials at launch, the rest as teams demonstrate need.

## Workspace structure

The workspace is organised into Projects, one per team or function.

**Team Projects** (day-to-day work)
- SEIS
- EIS / Scale-Up
- Business Development
- Operations
- Direct Deals / Cap Intros

**Function Projects** (cross-team work)
- Investor Relations
- Compliance
- Communications & Marketing

**Shared Workflow Projects** (used by multiple teams)
- Investment Memos (SEIS + EIS)

Each Project has its own knowledge files (from Drive), custom instructions, and a named owner. Recurring workflows are codified as Skills, called from inside the relevant Project.

## Purpose of this repo

Version control and source of truth for Claude Team **configuration** — system prompts, Skills, templates, connector setup. Not for content, knowledge, or day-to-day work.

The rule: configuration changes happen here first (committed with a reason), then get copied into the live workspace. Workspace and repo should never drift.

## Repo layout

    projects/      System prompts and custom instructions per Project
    skills/        Definitions for proven, repeatable workflows
    templates/     Output formatting templates
    mcp/           Connector setup guides and Integrations Register
    CHANGELOG.md   Log of meaningful config changes

## What does NOT live here

- Handbook, FAQ, guides → Google Drive (`Fuel AI Operations` Shared Drive)
- Knowledge / KB files → Google Drive
- Day-to-day work → Claude Team workspace

This repo is for **configuration and version control only**. Most of the team will never open it.

## Three-layer model

- **Configuration** — lives in this repo — audience: admins and champions
- **Knowledge & content** — lives in Google Drive — audience: whole team
- **Work** — lives in the Claude Team workspace — audience: whole team

## Status

**Early stage.** Claude Team is live and rollout is underway. This repo will be populated with real configuration as workflows prove themselves in use — not pre-built speculatively.

## Governance

- **Owner:** Michael Burnett
- **Contributors:** Champions (one per team) via PR
- **Review cadence:** Monthly review of Projects and Skills; quarterly review of integrations and access

## Related docs

- Rollout plan → Google Drive (`Fuel AI Operations`)
- Fuel AI Handbook → Google Drive (`Fuel AI Operations`)
- Integrations Register → `/mcp/README.md`
- Change log → `CHANGELOG.md`
