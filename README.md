# crypto-desk

Private trading desk for discretionary crypto on Robinhood. Cursor agents
read [`.cursor/skills/crypto-trading/SKILL.md`](.cursor/skills/crypto-trading/SKILL.md)
when placing, sizing, or managing a crypto trade.

This is **not** the Occasion Speech Writer. That product stays in
[`Acaydia/quickie`](https://github.com/Acaydia/quickie) at the repository root.

## Layout

| Path | What it is |
| --- | --- |
| `.cursor/skills/charles-clearance/SKILL.md` | Live-book proxy. Charles is the leader; every place/cancel/replace is cleared through Charles. |
| `.cursor/rules/charles-clearance.mdc` | Always-on rule for the same law. |
| `.cursor/skills/crypto-trading/SKILL.md` | Operational methodology. Sections 1–6 are distilled from trader transcripts. Section 7 is measured against the Robinhood API. |
| `research/crypto-trading-methodology-sources.md` | Source corpus and quotes behind sections 1–6. |
| `research/plan-reconciliation-2026-09-20.md` | Reconciliation of the 20 Sep 2026 plan against live book and fills. |
| `research/trade-plan-2026-09-21.md` | Monday 21 Sep 2026 trade plan. |
| `research/charles-clearance-2026-09-21.md` | Decision record: Charles is the clearance proxy. |

## Standing law

**Charles is the leader. Everything has to be cleared through Charles.**
Charles is the live-book proxy. No live order, cancel, or replace without
Charles's explicit clearance of that ticket. Details:
[`.cursor/skills/charles-clearance/SKILL.md`](.cursor/skills/charles-clearance/SKILL.md).

**Never guess.** No price level, stop, size, or capability claim goes into an
order unless it traces to something measured. Absence has to be demonstrated
by a call that failed, not inferred from a missing tool name.

Sells fill against the **bid**, not the mark. Crypto has no OCO: a take-profit
reserves units and cannot coexist with a stop.

## Licence

[MIT](LICENSE).
