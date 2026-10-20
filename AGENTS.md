# Working in this repo (humans and agents)

A concise "where to look" and the working boundaries. Authoritative detail lives in the
linked docs, not here.

## Where to look

| You want | Read |
|---|---|
| What ako is and why | `README.md`, `VISION.md` |
| How a session actually works | `docs/concept.md` |
| What we most need help on | `docs/get-involved.md` |
| The plan and its stages | `ROADMAP.md` |
| How feedback is handled | `TRIAGE.md` |
| How we work | `CONTRIBUTING.md` |

ako is at the idea stage: there is no application code yet. When there is, this table
gains an entry for it and the build steps move into `CONTRIBUTING.md`.

## Working boundaries

- Stay in the stated scope of a change; put anything else in the tracker.
- Update docs in the same change as the thing they describe.
- British English, no emojis, commas over em dashes, headings instead of horizontal
  rules. Conventional Commits for messages.

## Protected principles (from `VISION.md`)

- **Coach, never control.** ako never actuates, stops, or starts the machine. No feature
  may require it to.
- **The operator stays the thinker.** Where perception is unreliable, defer to the human
  rather than guessing.
- **Safety is certified first.** Cutting stays locked until a camera-verifiable
  machine-control certification is passed.
- **Fail safe.** On any uncertain or occluded reading, withhold approval and ask the
  human. Never reassure on uncertainty.

## Attribution policy

**Strip per-commit AI trailers; disclose AI assistance once.** No `Co-Authored-By:
Claude` or "Generated with Claude Code" lines in commit messages or pull requests.
Enforced mechanically: the `.githooks/commit-msg` hook rejects them at commit time
(install with `git config core.hooksPath .githooks`), and CI re-scans each push's new
commits (`scripts/check/ci-no-ai-trailers.sh`). The single disclosure lives in
`README.md`:

> ako is created by Vernon Kay with heavy use of AI assistance (Claude Code). The
> decisions and responsibility are the author's; the AI is a tool, disclosed here rather
> than credited per commit.
