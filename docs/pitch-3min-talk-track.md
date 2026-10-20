# One-Way Door: three-minute pitch, talk track

Slides: `docs/onewaydoor-pitch-3min.pdf` (five slides). Each slide's top bar shows where you should be on the clock.
About 430 words in total, which is three minutes at a calm pace.

## 1 · The question (0:00–0:30)

Every merge is a door. Most swing both ways: if the release goes wrong, you roll back and the old code carries on.
Some only open one way. They leave data behind that the old code can't handle, so rollback doesn't save you.
One-Way Door is a GitHub Copilot skill that asks, before you merge: if this goes wrong after deploy, can we actually
roll back?

## 2 · The problem (0:30–1:10)

Here's how it goes wrong. A release changes a table, an event or a stored format. New data gets written. Something
breaks, and the plan is to roll back. But only the code goes back; the data stays. Now old code meets new data. It
fails to start, or worse, it starts and quietly gets things wrong.

It happens in four places: databases, events, caches and external contracts. In our demo, one rollback booked fifty
settlements at zero pounds, and twelve thousand pounds went missing, with every dashboard green. Tests, CI and code
review all look forward. None of them runs the old code against the new data.

## 3 · The skill (1:10–1:50)

The fix is one folder in your repository. Copilot loads it when a pull request touches a migration or an event, or
when someone asks whether they can roll back.

It does four things. It classifies each change as two-way or one-way. It says when the door closes and what breaks.
It finds the blast radius, including code outside the PR. And it proposes a safe split. Small offline scripts check
the facts; Copilot does the judgement. On our demo PR it said one-way, no safe window, and named finance's job,
which wasn't in the PR. Every prediction matched a real failure when we ran it.

## 4 · The concepts (1:50–2:25)

Four ideas. Two-way or one-way. When the door closes: here, the five milliseconds it takes a migration to run. The
blast radius: every reader of the data, where the one that breaks first is often not in the diff. And the split:
expand, migrate, contract, drop. The same change in four deploys, each reversible. We proved it: all four steps pass
a real rollback test, and the original PR fails before anyone even presses rollback.

## 5 · Where it applies (2:25–3:00)

It works anywhere data outlives code: SQL migrations in Flyway, Liquibase or EF Core, event schemas, caches, keys
and partner contracts. It runs everywhere Copilot does: VS Code, the CLI, the cloud agent and code review. It
protects authors, reviewers, on-call and finance. Adopting it is one copy command; it needs no servers and makes no
network calls. Know before you merge whether you can roll back.
