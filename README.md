# Slack Incident Commander

A Slack-native incident response agent for security and operations teams.

Slack Incident Commander helps responders triage alerts, gather context through tools, coordinate tasks, maintain a timeline, and draft incident updates from inside Slack.

This repository is being built for the Slack Agent Builder Challenge as a portfolio-grade agentic operations project.

## Current Status

Initial project spine. The first target workflow is a synthetic security incident involving suspicious Slack OAuth activity.

Start with [docs/START_HERE.md](docs/START_HERE.md) and [docs/BRAINSTORMING.md](docs/BRAINSTORMING.md).

## Core Workflow

1. A responder invokes the agent with an incident alert.
2. The agent normalizes and triages the alert.
3. Tool calls gather identity, audit, and event context.
4. The agent posts an incident brief with severity, confidence, affected assets, and next actions.
5. The agent tracks responder tasks and timeline events.
6. The agent drafts stakeholder updates and a postmortem.

## Repository Layout

```text
docs/          Product, architecture, demo, and submission notes
src/app/       Slack app entry points and interaction handlers
src/domain/    Incident domain model and orchestration logic
src/tools/     Deterministic local tools used by the agent
src/mcp/       MCP server adapter for tool access
src/demo/      Synthetic demo scenarios
tests/         Unit and behavior tests
scripts/       Local development and demo helpers
```

## Development

The implementation will use TypeScript and Node.js. Setup instructions will be finalized once the Slack app scaffold and local MCP server are wired.

Recommended model level for ordinary repo work: **High**. Use **Medium** for docs-only updates and **Very High** for final review, difficult debugging, or submission polish.

Run the deterministic local demo:

```bash
npm run demo
```

Run tests:

```bash
npm test
```

## Slack App

The initial Slack app manifest draft is in `slack/manifest.yaml`. It will be refined after the sandbox app is created and tested.

Slack setup instructions are in [docs/SLACK_SETUP.md](docs/SLACK_SETUP.md).

## License

MIT.
