# One-Way Door: speaker notes, 180 seconds

For the five-page document `docs/onewaydoor-problem-and-solution.pdf`: one script per page, with page 5, the payoff,
given the most time.

- **Length:** about 400 spoken words, which is 2 minutes 50 at a calm 140 words a minute.
- **Cues:** **[next]** means move to the next page. **[pause]** means a one-second beat; let the line land.
  Bold words are the ones to lean on.
- **The scenario is invented:** Northwind Payments, its customers and its amounts. The values and purpose are
  Lloyds Banking Group's own.

| Page | Topic | Clock |
|---|---|---|
| 1 | In short | 0:00–0:30 |
| 2 | The scenario | 0:30–1:05 |
| 3 | Today's safety nets | 1:05–1:35 |
| 4 | What's different | 1:35–2:05 |
| 5 | The skill in action | 2:05–3:00 |

---

## Page 1 · In short (0:00–0:30)

> Everyone here works to one purpose: **Helping Britain Prosper.**
> And behind every payment we move is a person. **[pause]**
>
> Here's the uncomfortable truth about our safety net.
> **Rollback restores the code. It can't restore what the code already did.**
>
> One-Way Door is a GitHub Copilot skill that spots those changes **before we merge**,
> and shows us how to ship them safely.

*Delivery: say the bold line slowly, then look up. It's the line people should remember.*

**[next]**

## Page 2 · The scenario (0:30–1:05)

> Picture a simple payment. **Customer A pays customer B**, through three small services and the bank network.
> It works every day.
>
> Then version two of the routing service goes live. Tests pass. Stage is green.
> But it reads the wrong account ID, and A's money starts going to **customer C.** **[pause]**
>
> By the time B calls asking where their money is, **a hundred and twenty payments** have gone.
> **Forty-eight thousand pounds.** Under the Consumer Duty, that's **foreseeable harm.**
>
> We roll back in five minutes. The code is fixed. **Not one payment comes back.**

*Delivery: trace the arrow from A to C on the second diagram with your hand.*

**[next]**

## Page 3 · Today's safety nets (1:05–1:35)

> And our teams **did everything right.** Backups. Production readiness on stage.
> Regression and smoke tests. Rollback drills. Canary releases. Monitoring.
> **All of them passed.**
>
> These are strong safety nets, and they're aimed at the **code and the platform.**
> None of them asks the one question that mattered:
> **does this change do something we can't take back?**

*Delivery: credit the teams warmly. This is respect for their work, not criticism of it.*

**[next]**

## Page 4 · What's different (1:35–2:05)

> That's the question One-Way Door asks, **on every pull request, before anyone deploys.**
>
> It classifies each change as **two-way or one-way.** It says **when the door closes.**
> It finds everyone who relies on the data, including teams outside the PR.
> That's our **Inclusive** value, in code.
>
> And it's honest about its limits. It doesn't claim to catch every bug.
> It makes sure a bug **can't become final.** That's **Trust**: we explain our reasoning.

*Delivery: point to "What it doesn't claim". Admitting the limits earns trust.*

**[next]**

## Page 5 · The skill in action (2:05–3:00)

> Here's the same change, with the skill. Copilot flags it: **one-way.**
> The door closes at the **first payment sent to the bank.** There's no safe rollback window.
>
> So it proposes a safer route. First, version two runs **in shadow**: it works out the payee,
> but version one still pays. Then we **compare.**
> Every one of A's payments shows a mismatch. **[pause]**
>
> **Caught. Zero pounds moved.** No recall, no incident, no late-night fixes, no customer let down.
>
> That's **Bold**, done safely. That's **People-First**: customers never pay for our mistakes.
> And it's **Trust**, the thing a bank runs on. **[pause]**
>
> Rollback restores the code. **One-Way Door protects what the code does.** Thank you.

*Delivery: point to "£0" in the final table. Slow right down for the last two lines.*

---

## How the values map to the story

| Value or principle | Page | The line |
|---|---|---|
| **Helping Britain Prosper** (purpose) | 1 | “Behind every payment we move is a person.” |
| **Consumer Duty**: avoid foreseeable harm | 2 | “Under the Consumer Duty, that's foreseeable harm.” |
| **Trust**: honest, explain our decisions | 3, 4 and 5 | Credit the teams; “we explain our reasoning”; “the thing a bank runs on.” |
| **Inclusive**: seek out diverse perspectives | 4 | “It finds everyone who relies on the data, including teams outside the PR.” |
| **Bold**: innovate and take action | 5 | “Bold, done safely.” |
| **People-First**: go further for customers | 5 | “Customers never pay for our mistakes.” |
| **Sustainable**: take responsibility for our impact | 5 | “No recall, no incident, no late-night fixes.” |

## If you're running over

Cut these, in this order, and you'll save about 25 seconds:
1. Page 3: “Backups. Production readiness on stage. Regression and smoke tests. Rollback drills. Canary releases.
   Monitoring.” Keep “All of them passed.”
2. Page 2: “It works every day.”
3. Page 5: “No recall, no incident, no late-night fixes, no customer let down.” Keep “Caught. Zero pounds moved.”

## Three likely questions, with one-line answers

- **“Couldn't a test have caught the wrong payee?”** A good one could. This makes sure that when a test misses it,
  the bug shows up in shadow, before money moves.
- **“Doesn't our release process already cover this?”** It covers the code going forward and back. This covers what
  the code already did, and it acts before merge.
- **“Will it block our pull requests?”** No. It reviews and explains; people decide. It never changes code unasked,
  and no data leaves the bank.

## Sources

- Lloyds Banking Group values: People-First, Bold, Inclusive, Sustainable, Trust, from the Group's
  [Code of Ethics and Responsibility (2024)](https://www.sec.gov/Archives/edgar/data/1160106/000116010625000005/lbgexhibit1122024.htm)
  and its [careers site](https://lloydsbankinggrouptalent.com/why-lbg/our-values/).
- Purpose: Helping Britain Prosper, from the same Code.
- Consumer Duty: the FCA's cross-cutting rule to avoid causing foreseeable harm to retail customers.
