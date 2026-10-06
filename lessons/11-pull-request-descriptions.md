---
title: Writing Pull Request Descriptions
summary: Write pull request descriptions that help reviewers understand, test and approve your changes.
date: 2026-10-06
---

## Why this matters

A pull request (PR) is a request for someone else's time. A good description tells the reviewer what changed, why, and how to check it, so they can review faster and give better feedback. It also becomes documentation: people will read your PR when they search for why the code works the way it does.

## The core skill

### The structure

Most good PR descriptions have four sections:

1. **What:** a short summary of the change.
2. **Why:** the problem or the ticket.
3. **How to test:** steps the reviewer can follow.
4. **Notes:** anything the reviewer should pay attention to.

```text
Title: Add CSV export to the reports page

## What
Adds an "Export CSV" button to the reports page. The export uses
the same filters as the table.

## Why
Customers asked to analyze reports in Excel. Closes #512.

## How to test
1. Go to /reports and set a date filter.
2. Click "Export CSV".
3. Check that the file has the same rows as the table.

## Notes
- Exports are limited to 10,000 rows for now. Larger exports will
  need a background job (follow-up ticket: #530).
- The main logic is in reports/export.ts. The other files are small changes.
```

The PR title usually follows the same rules as a commit subject: imperative and specific.

### Describing the change

In the "What" section, you can use the present simple to describe what the PR does. The PR is the subject, so the verb ends in *-s*:

```text
This PR adds a CSV export.
It also renames ReportTable to ReportsTable.
```

You can also write short bullet points with no subject: *Adds export button. Renames ReportTable.*

### Guiding the reviewer

Reviewers don't know which parts are important. Tell them.

```text
The main change is in billing/invoice.ts. Everything else is renaming.
I'm not 100% sure about the caching approach. Feedback welcome!
Screenshots of the new modal are below.
```

If the PR is not ready, mark it as a draft and say what's missing: *Draft: tests are still missing.*

### Explaining decisions

If you chose one solution over another, explain briefly. This prevents long discussions in the comments.

```text
I used a database index instead of caching, because the data changes
often and caching would show old values.
```

## Useful phrases

**Summary**

- **This PR adds / fixes / removes** …
- **This is part of** the checkout redesign.
- **Closes** #512. / **Follow-up to** #498.

**Testing**

- **To test,** run `npm run seed` and log in as admin.
- **I've tested this** on Chrome and Safari.
- **Added unit tests for** the edge cases.

**Guiding reviewers**

- **The interesting part is** in parser.ts.
- **Most of the diff is** generated code.
- **I'd especially like feedback on** the error handling.
- **Out of scope:** the mobile layout. I'll do it in a separate PR. (*out of scope* = not included in this work)

**Status**

- **Ready for review.**
- **WIP**, please don't merge yet. (*WIP* = work in progress)
- **Depends on** #520.

## Common mistakes

**"This PR add a new endpoint."**
With *this PR* (third person singular), the verb needs *-s*: *"This PR **adds** a new endpoint."*

**"Please review."**
This is the only line of the description. Add what, why and how to test: *"**Adds rate limiting to the login endpoint to stop brute-force attacks. To test, …**"*

**"I have make some changes in the API."**
After *have*, use the past participle: *"I have **made** some changes to the API."*

**"Fixed the things from the meeting."**
The reader may not have been at the meeting. Name the changes: *"**Fixed the date format and the empty-state message**, as discussed with the design team."*

## Formal vs. casual

- **Open-source project or another team's repo:** "Thanks for maintaining this library! This PR fixes a crash when the config file is empty (#87). I've added a test that reproduces the issue. Happy to make any changes."
- **Your own team's repo:** "Fixes the empty config crash (#87). Test included. Small one!"

When you contribute to someone else's project, be extra clear and polite, because the maintainers don't know you.

## Exercise

Choose a PR you opened recently, or a change you're working on now. Write a full description with What, Why, How to test and Notes. Include at least one sentence that guides the reviewer to the most important part.

*Hint:* imagine the reviewer is a new team member who doesn't know the ticket. Could they test your change using only your description?

## Recap

- Use the sections What, Why, How to test and Notes.
- Write the title like a commit subject: imperative and specific.
- Use *This PR adds…*, with *-s* on the verb.
- Tell reviewers where the important changes are.
- Explain your decisions to avoid long comment threads.
