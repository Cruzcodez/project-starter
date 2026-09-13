# Repository structure

```
.
├── .github/
│   ├── workflows/ci.yml            # runs scripts/check.sh, nothing else
│   ├── ISSUE_TEMPLATE/task.md
│   └── pull_request_template.md
├── .kiro/steering/                 # standards agents must follow
├── docs/
│   └── decisions/                  # ADRs, numbered, immutable
├── scripts/check.sh                # the single health command
├── src/                            # application code
├── tests/                          # tests
├── AGENTS.md                       # working agreement + definition of done
├── README.md                       # problem, scope, architecture, limits
├── LICENSE
└── .gitignore
```

## Rules

- `src/` holds code. `tests/` holds tests. Don't interleave them.
- Infrastructure as code, when present, goes in `infra/`.
- **One README.** Not `README.md` plus `SETUP.md` plus `NOTES.md` plus `GETTING_STARTED.md`. Documentation sprawl is how documentation stops being read.
- **One CHANGELOG**, if the project is released at all. A POC usually isn't.
- Scratch files, experiments, and notes-to-self do not belong in the repository. That's what a local directory outside the repo is for.

## Adding a directory

New top-level directories need a reason that fits in one sentence. If the reason is "it seemed tidier," don't.
