# <Project Name>

> One sentence: what this does and who it's for. Replace this line first.

## Problem

What was actually broken or missing. Not the solution — the situation that made this worth building.

## Scope

**In scope**

- 

**Out of scope**

- 

Being explicit about what you deliberately did *not* build is the difference between an unfinished project and a scoped one.

## Architecture

How it's put together, and why that way. A diagram helps; a paragraph is the minimum.

## Running it

```bash
# prerequisites

# install

# run
```

## Testing

```bash
./scripts/check.sh
```

What's covered, what isn't.

## Limitations

Known gaps, rough edges, things that will break under load. Write these down honestly — a reader who finds a limitation you didn't disclose stops trusting the whole document.

## If this went to production

What you'd change. Auth, secrets handling, scaling, monitoring, cost, failure modes.

---

## Setup checklist

Delete this section once you've worked through it.

- [ ] Replace the title and one-liner above
- [ ] Fill in Problem and Scope **before** writing code
- [ ] Update `LICENSE` with the current year and your name
- [ ] Replace the placeholder block in `scripts/check.sh` with real checks
- [ ] Fill in `.kiro/steering/tech.md` with this project's actual stack
- [ ] Write the first ADR in `docs/decisions/`
- [ ] In repo settings: enable Dependabot, and add a ruleset on `main`
- [ ] Delete `docs/templates/` — you don't need it anymore
