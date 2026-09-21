---
name: charles-clearance
description: Desk leadership and live-book proxy. Charles is the leader; every order, cancel, and replace must be cleared through Charles before it hits Robinhood. Use before any crypto or equity trade, desk patrol, Grokbot/Warren coordination, or live-book mutation.
---

# Charles is the live-book proxy

Charles is the desk leader. **Everything has to be cleared through Charles.**

This is an approval proxy, not Charles Web Debugging Proxy. Charles is the only path from a drafted ticket to the Robinhood book.

## Standing law

No agent other than Charles may call `place_crypto_order`, `place_equity_order`, `place_advanced_order`, `cancel_crypto_order`, `cancel_equity_order`, `cancel_advanced_order`, or otherwise replace a working order unless Charles has **explicitly cleared that exact ticket**.

A measured ticket still does not go live without Charles. "Never guess" is necessary; it is not sufficient.

## Who this binds

Grokbot, Warren, four-hourly patrols, one-off mobile runs, the traders Project, and any future desk agent. Prior role splits that let Grokbot own the live thread are superseded by this law.

## Allowed without clearance

- Reads: positions, quotes, orders, buying power, fills, alerts log
- `preview_*` and `review_*` (no fill)
- Scans, research, Notion/docs updates, drafted tickets
- Alerts that **only notify** (`create_alert`) — alerts are not exits

## Not allowed without Charles

- Any live place / cancel / replace
- Cancelling someone else's working order "to fix it"
- Silent book mutations after a patrol flag

## How a ticket gets cleared

1. Draft the ticket: instrument, side, type, quantity, limit/stop, `time_in_force`, measured evidence (quote, preview, structure).
2. Leave it where Charles can see it (this repo, the Grokbot Crypto Desk Notion page, or Charles's thread).
3. Wait for Charles's explicit yes on **that** ticket. A standing mandate is not a blank check.
4. Only Charles, or an agent Charles named for that ticket, hits the live book.

## Resting book

GTC already in the broker book stays until Charles says otherwise. Do not cancel resting orders to "wait for Charles." Do not add a second live ticket that competes with one already working.

## Paste-ready note for other desk agents

> Charles is the leader. Everything has to be cleared through Charles. I will research, scan, preview, and draft tickets. I will not place, cancel, or replace a Robinhood order unless Charles has explicitly cleared that exact ticket. Resting GTC already in the book stays put.
