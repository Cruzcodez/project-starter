# 3. Scope

**Date:**
**Confirmed with:** _name, and the date they agreed_

Only write this file if `02-discovery.md` came back "build it" or "build something smaller."

That line at the top about who confirmed it is the most important line in this folder. A scope document nobody agreed to is a diary entry. You'll still have the argument, you'll just have a piece of paper to wave during it.

Send it. Get a reply. Write down the name and the date. If it's your own project, "confirmed with: me, 14 Sep" still counts, because now there's a version of you on record.

---

## What we're building

Two or three sentences. If you can't explain it that briefly, you don't have scope yet, you have a vibe.

> 

## In scope

The things you're actually building. Be specific enough that both of you would agree on whether each one is finished.

- [ ] 
- [ ] 
- [ ] 

## Out of scope

This is the section that does the work, so don't rush it.

It is not a list of refusals. It's a parking lot. "We could also have it write to their calendar" is a perfectly good idea. Putting it here means you get to have the idea without it eating the project, and the next conversation starts with "we already spotted that, it's phase two" instead of you quietly building it at 11pm on a Tuesday.

Write down anything that came up and isn't being built. Include the obvious ones. The obvious ones are exactly where people's assumptions differ.

- 
- 
- 

## Acceptance criteria

How everyone agrees it's done. Each one should be something you can go and check.

Write these as things a person does, not as things the system has.

Weak: "the search works."
Better: "a user types a policy name and gets the right document in the top three results."

- [ ] 
- [ ] 

## Not production ready

Say this here as well as in the handoff. Once isn't enough, and this is the document people actually read.

This is a proof of concept. It exists to answer a question, not to be run for real. Before anyone puts it in front of users it needs, at minimum:

- 
- 

## What happens when scope changes

It will. That's fine and normal. What isn't fine is it changing quietly.

When something new comes up:

1. Write it down here, under Out of scope
2. Decide together whether it replaces something in scope or extends the timeline
3. Update the date and the confirmed-with line

Adding work without adjusting either the scope or the schedule is how a two week proof of concept turns into two months and nobody can point at when it happened.

---

## Prompt for your AI assistant

Use this one to pressure test your scope before you send it. Vague scope is worse than no scope, because vague scope makes everyone feel protected while protecting nobody.

```
Here's the scope document for a proof of concept:

[paste 03-scope.md]

Review it like someone who will have to argue about it later. Specifically:

- Which in-scope items are vague enough that two people could disagree about
  whether they're done? Quote them and say what's ambiguous.
- Which acceptance criteria can't actually be checked? Rewrite them as
  something a person could go and verify.
- What's obviously adjacent to this work and missing from the out-of-scope
  list? That gap is where the argument happens later.
- Is anything in scope that discovery didn't justify?

Be blunt. Don't tell me it looks good. Find the parts that will cause a
problem in six weeks.
```
