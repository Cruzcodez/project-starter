# project-starter

A GitHub template repository. Click **Use this template** and you get a new repo that already has continuous integration, a secret scan, a working agreement for AI coding agents, and a place to record decisions — so none of that gets re-derived from scratch at the start of every project.

It is built for small, focused work: proofs of concept, internal tools, customer deliverables. It is deliberately minimal. If a project outgrows it, that is a signal to add what *that* project needs — not evidence this template was missing something.

## Using it

1. Click **Use this template → Create a new repository**
2. Clone it, then replace this README with the project skeleton:
   ```bash
   cp docs/templates/README.md README.md
   rm -r docs/templates
   ```
3. Fill out `engagement/01-intake.md` before writing any code. It's the one that stops "I thought this was also going to do X" six weeks later.
4. Work through the setup checklist at the bottom of that new README
5. In the new repo's **Settings**, enable Dependabot and add a ruleset on `main`

Step 5 catches people out. GitHub's template feature copies *files*, not *settings* — branch protection, Dependabot, and merge rules do not come along, and a repo without them is a repo where nothing stops you.

## What's in here

| Path | What it is | Who reads it |
| --- | --- | --- |
| `scripts/check.sh` | The single health command. Scans for tracked credential files, then runs the project's own lint and tests. | you, CI |
| `.github/workflows/ci.yml` | Runs `check.sh` on every pull request and push to `main`. Nothing else. | CI |
| `.github/dependabot.yml` | Weekly dependency updates, grouped, with a low PR limit. | Dependabot |
| `AGENTS.md` | Working agreement and definition of done for coding agents. | Claude, Kiro, any agent |
| `.kiro/steering/` | Code standards, repo structure rules, and per-project tech constraints. | agents, you |
| `engagement/` | Intake, discovery, scope, and handoff. The thinking behind the project, in four files, each ending with an interview prompt for an AI assistant. | you, the customer, whoever inherits it |
| `docs/decisions/` | Architecture decision records. Numbered, immutable, short. | whoever inherits this |
| `.github/pull_request_template.md` | Forces every PR to state why, how to verify, and what the risk is. | reviewers |
| `.github/ISSUE_TEMPLATE/task.md` | Forces every task to state acceptance criteria and what is out of scope. | you |
| `.gitignore` | Matches every `.env` variant, not just the narrow framework default. | git |
| `docs/templates/README.md` | The README skeleton for a generated project. Delete after copying. | you, once |

## The one idea worth understanding

**`scripts/check.sh` is the only health command, and CI runs exactly that file.**

The moment CI grows steps that do not exist in `check.sh`, "passes on my machine" and "passes in CI" stop meaning the same thing, and you start debugging the pipeline instead of the code. One command, both places, no drift.

It also scans for tracked credential files on every run. `.gitignore` is not retroactive — once a file is committed, ignoring it does nothing — so the scan catches what the ignore rules could not.

## Conventions this template assumes

- **Conventional commits** — `feat:`, `fix:`, `chore:`, `docs:`, `test:`, `refactor:`
- **Branches named `type/short-description`**, using the same vocabulary as commit types
- **Pull requests for everything**, squash-merged, so one PR becomes one commit on `main`
- **ADRs for decisions that constrain future work** — datastore, auth model, deployment target, a deliberate omission. Not for preferences with no downstream cost; those belong in `.kiro/steering/`.

## What this deliberately leaves out

No CHANGELOG — a proof of concept is not released. No CONTRIBUTING or CODEOWNERS — they describe a team that does not exist yet. No reusable workflow library — extraction comes *after* repetition, once you know what actually varies.

Each of those is a file that exists to look professional rather than to do work. Add one the day something needs it.

## License

MIT. See [LICENSE](LICENSE).
