# Charles clearance — 21 Sep 2026

## Decision

Charles is the desk leader. Everything has to be cleared through Charles.

Charles is the live-book **proxy**: every place, cancel, and replace must be explicitly cleared by Charles before it hits Robinhood.

## Source

Two consecutive mobile runs on 21 Sep 2026:

1. "Cursor , Charles is the leader" (run name: Cursor leader context)
2. "Everything has to be cleared through Charles" (run name: Charles proxy setup)

This is not Charles Web Debugging Proxy. It is an approval proxy for the trading desk.

## What it supersedes

Earlier desk notes let Grokbot own the live Robinhood thread and execute without a second clearance. That is no longer true. Grokbot, Warren, patrols, and other agents may still research, scan, preview, and draft tickets. They do not hit the live book unless Charles clears the ticket.

"Never guess" still applies. A measured ticket is not an exception to Charles.

## Resting book

Orders already working as GTC stay until Charles says otherwise. Do not cancel them to wait for clearance. Do not place a competing ticket on the same units.

## Where this lives

- Skill: `.cursor/skills/charles-clearance/SKILL.md`
- Always-on rule: `.cursor/rules/charles-clearance.mdc`
- `AGENTS.md`
- README standing law
- Notion: Grokbot Crypto Desk

Home repository is `Acaydia/crypto-desk`. Do not add this to `Acaydia/quickie` (speech writer).
