# Lineup Builder — Criteria Guide (ALL / ANY)

> **The most granular filtering lineup creator out there** — it builds a full lineup straight
> from the cards *you actually own*, narrowed to the exact traits a program or event is asking
> for, with complete control over how every requirement combines.

A quick, plain-English guide to building filters in the **Lineup Builder** tab. Anyone can
follow this — there's really just one idea (**ALL / ANY**), used in two places.

## The whole system in one picture

Your criteria are a stack of **lines**. There are only **two switches**, and they use the
same word both times:

```
Card must match  [ ALL / ANY ]  of the lines below     ← top switch
┌─────────────────────────────────────────────┐
│ [ ALL / ANY ]  Pitcher   and   Sinker   and   Cutter │   ← line 1 (its own switch)
└─────────────────────────────────────────────┘
                      AND  /  OR                          ← set by the top switch
┌─────────────────────────────────────────────┐
│ [ ALL / ANY ]  Age 35+   or   Vintage   or   Live    │   ← line 2 (its own switch)
└─────────────────────────────────────────────┘
```

### 1. Each line's switch — ALL or ANY
- **ALL** → a card must match **every** criterion on that line. (shown joined by **and**)
- **ANY** → matching **any one** criterion on that line is enough. (shown joined by **or**)
- Add more criteria to a line with **+ add**. Start a new line with **+ Add line**.

### 2. The top switch — ALL lines or ANY line
- **ALL lines** → a card must satisfy **every** line. (lines joined by **AND**)
- **ANY line** → satisfying **any one** line is enough. (lines joined by **OR**)

A card **qualifies** when it satisfies the top switch. (Criteria that don't apply to a card —
like a pitching rule on a hitter — are simply skipped for that card.)

## Showing results
- By default the **Spare Players** list shows everything, with qualifying cards sorted to the top.
- Tick **Only show matches** to hide cards that don't qualify — a clean list of eligible players.
- **Programs grind vs Events** only changes how Auto-build *ranks* the qualifying players
  (Programs: matching more is better; Events: any match counts, then best OVR).

## Worked examples

### The event: a sinker+cutter pitcher who is also 35+, Vintage, or Live
`(Pitcher AND Sinker AND Cutter) AND (35+ OR Vintage OR Live)`

| | |
|---|---|
| **Top switch** | **ALL lines** |
| **Line 1** | **ALL** of: `Pitchers only` · `Throws pitch: Sinker` · `Throws pitch: Cutter` |
| **Line 2** | **ANY** of: `Age older than 35` · `Card type: Vintage` · `Card type: Live` |

✅ Sinker+cutter pitcher, age 37 → qualifies
✅ Sinker+cutter pitcher, age 28, Live → qualifies
❌ Sinker+cutter pitcher, age 28, Diamond → excluded (fails line 2)
❌ Pitcher with sinker but no cutter → excluded (fails line 1)
❌ Any hitter → excluded (fails line 1)

### Any lefty masher, OR any burner
`(bats Left AND Power 100+) OR (Speed 95+)`

| | |
|---|---|
| **Top switch** | **ANY line** |
| **Line 1** | **ALL** of: `Bats: L` · `Power ≥ 100` |
| **Line 2** | **ALL** of: `Speed ≥ 95` |

### Live Series catchers
`Live AND position C` — one line, so the top switch doesn't matter.

| | |
|---|---|
| **Line 1** | **ALL** of: `Card type: Live` · `Position: C` |

## Cheat sheet
- One requirement with alternatives → put the requirement on its own **ALL** line, put the
  alternatives on an **ANY** line, set the top switch to **ALL lines**.
- A few totally separate "any of these is fine" profiles → one line each, top switch **ANY line**.
- Saved filters/builds remember both switches; old saved filters load as **ANY line** with **ALL** lines.
