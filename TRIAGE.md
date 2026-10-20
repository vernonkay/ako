# Triage and feedback playbook

How feedback moves from "someone said something" to "handled, with a reply". The promise:
**every issue and discussion gets a human response**, even when that response is a warm
"thank you, but no".

## Where things land

- **Concrete proposals and problems to track** go to GitHub **Issues** (via the issue
  forms).
- **Questions, open-ended ideas, show-and-tell** go to GitHub **Discussions**.
- **A way the design could mislead a learner into an unsafe action** is treated as a
  priority, see [`SECURITY.md`](SECURITY.md).

Blank issues are disabled, so everything arrives shaped for triage.

## The label model, a decision encoded

Every new issue opens with **`needs-triage`**. Triage means replacing that with a
decision:

- **Area** one of `a:safety`, `a:perception`, `a:curriculum`, `a:framework`, `a:docs`.
- **Outcome** exactly one of:

| Label | Means | Then |
|---|---|---|
| `accepted` | We will do it; it fits the roadmap | Note it on the roadmap, keep open |
| `backlog` | Agreed in principle, not now | Keep open, no timing commitment |
| `needs-info` | Cannot act without more detail | Ask; stale-bot closes if it goes quiet |
| `duplicate` | Already tracked | Link the original, close |
| `wontfix:scope` | Out of scope for now | Explain, close kindly |
| `wontfix:vision` | Pulls against a non-goal | Explain, link VISION, close kindly |

`good first issue` and `help wanted` go on anything a contributor could pick up.

## Tone

Every reply, including every "no", should leave the person glad they posted. Thank them,
be specific about why, point somewhere useful, and never make a decline feel like a
brush-off. A good "no" is part of the project.
