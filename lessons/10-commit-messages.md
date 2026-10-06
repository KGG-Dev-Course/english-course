---
title: Writing Good Commit Messages
summary: Write short, clear commit messages in the imperative mood that explain what changed and why.
date: 2026-10-06
---

## Why this matters

Your commit history is a diary of the project. Months later, someone (often you) will run `git log` or `git blame` to understand why a line of code exists. A good commit message answers that question in seconds. Commit messages are also one of the most common kinds of English that every developer writes, many times a day.

## The core skill

### The imperative mood

Most teams write the subject line in the imperative mood: the base form of the verb, like a command.

```text
Add retry logic to the payment client
Fix crash when the user has no avatar
Remove unused feature flags
```

A simple test: your subject should complete the sentence *"If applied, this commit will…"*

- *If applied, this commit will* **add retry logic to the payment client.** Correct.
- *If applied, this commit will* **added retry logic.** Doesn't work.

### The subject line

- Start with a capital letter and a verb.
- Keep it under about 50 characters.
- Don't end it with a full stop.
- Be specific: say what changed, not just which file.

Weak subjects and better versions:

```text
fix bug              ->  Fix timezone bug in the booking calendar
update               ->  Update Node.js from 18 to 20
changes to user.ts   ->  Validate email format on signup
```

### The body: explain why

For anything more than a tiny change, add a body after a blank line. The code shows *what* changed. The body explains *why*.

```text
Add retry logic to the payment client

The payment provider sometimes returns 503 during peak hours.
Without retries, these orders fail and customers have to pay again.

Retry up to 3 times with exponential backoff. Only retry on 502,
503 and 504, so we never charge a customer twice.

Fixes #318
```

In the body, use normal sentences in the present or past tense. Wrap lines at about 72 characters.

### Choosing the right verb

A few verbs cover most commits:

- **Add**: new feature, file or test.
- **Fix**: a bug.
- **Update / Upgrade**: change a version or existing content.
- **Remove**: delete code or features.
- **Refactor**: change structure without changing behavior.
- **Rename / Move**: change names or locations.
- **Improve**: make something faster or better.

Some teams use prefixes like *feat:*, *fix:* or *docs:* (Conventional Commits). The English after the prefix follows the same rules: *fix: handle empty search results*.

## Useful phrases

**Subject lines**

- **Add** pagination to the orders endpoint
- **Fix** memory leak in the image uploader
- **Handle** null values in the CSV parser
- **Prevent** duplicate emails on retry
- **Simplify** the auth middleware

**Body**

- **Previously,** the job ran every minute, which overloaded the database.
- **This change** moves the check to the server side.
- **This is needed for** the new reporting feature.
- **No behavior change.** (for refactors)

**References**

- **Fixes** #42 / **Closes** #42 (closes the issue on GitHub)
- **Related to** #57
- **Co-authored-by:** (for pair programming)

## Common mistakes

**"Added validation to the signup form"**
Use the imperative, not the past tense: *"**Add** validation to the signup form"*

**"Fixing the login bug"**
Use the imperative, not the *-ing* form: *"**Fix** the login bug"*

**"Fix bug"**
Grammatically fine, but useless. Say which bug: *"Fix **logout not clearing the session cookie**"*

**"Fix the bug which was making the dashboard to load slowly"**
After *make* + object, use the base verb without *to*: *"…which was making the dashboard **load** slowly"*. Shorter is even better: *"Fix slow dashboard loading"*.

## Formal vs. casual

Commit messages don't really have formal and casual versions, but different teams have different styles. Compare:

- **Open-source or large company style:** "Fix race condition in session refresh" with a full body explaining why.
- **Conventional Commits style:** "fix(auth): prevent race condition in session refresh"
- **Small team, small change:** "Fix typo in README"

Check your team's last 20 commits and match their style. Avoid jokes and messages like "wip", "asdf" or "final fix 2" on shared branches.

## Exercise

Run `git log --oneline -20` in a project you work on. Choose five commit messages and rewrite them using the rules from this lesson: imperative verb, specific, under 50 characters.

Then pick one of them and write a body of 2–3 sentences explaining *why* the change was made.

*Hint:* test each subject with "If applied, this commit will…"

## Recap

- Use the imperative mood: *Add, Fix, Remove*, not *Added* or *Fixing*.
- Keep the subject short, specific and without a full stop.
- Use the body to explain why, not what.
- Learn a few key verbs: *add, fix, update, remove, refactor*.
- Match your team's style.
