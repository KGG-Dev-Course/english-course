---
title: Giving a Daily Standup Update
summary: Give a short, clear standup update about yesterday, today and your blockers.
date: 2026-10-06
---

## Why this matters

In many teams, the daily standup is the only time you speak in English every day. It's short, but everyone is listening. A clear update helps the team plan, and it shows your progress without you having to "sell" your work.

## The core skill

### Yesterday, today, blockers

Most standups follow three questions:

1. What did you do yesterday?
2. What will you do today?
3. Is anything blocking you?

```text
Yesterday I finished the password reset flow and opened a PR.
Today I'm going to address the review comments and then start on
the email templates.
No blockers.
```

That's about 20 seconds. That's the right length.

### The right verb tenses

Each part has its own tense:

- **Yesterday:** past simple, because it's finished. *I fixed, I reviewed, I deployed.*
- **Today:** *going to* or present continuous for plans. *I'm going to write tests. I'm pairing with Jo.*
- **Blockers:** present simple or present continuous. *I'm waiting for access. The API keys don't work.*

If a task from yesterday isn't finished, use the present continuous or *still*:

```text
I'm still working on the cache bug. I found the cause, but the fix
is more complicated than I expected.
```

### Talk about results, not activity

"I worked on the ticket" says nothing. Say what changed.

- Activity: *I worked on the search API.*
- Result: *I added filters to the search API. Sorting is next.*

### Raising a blocker

A blocker is anything that stops your progress. Say what it is and who can help. Then discuss details after the standup.

```text
I'm blocked on the payment tests. I need access to the Stripe test
account. Kim, could you add me after the standup?
```

*After the standup* is important. Long discussions during the meeting waste everyone's time. People often say "let's take this offline", which means "let's discuss this later, with fewer people".

## Useful phrases

**Yesterday**

- **I wrapped up** the migration. (*wrap up* = finish)
- **I spent most of the day** debugging the flaky test.
- **I got the PR merged.**

**Today**

- **Today I'm going to** focus on the dashboard.
- **I'll pick up** the next ticket from the board. (*pick up* = start working on)
- **I'm pairing with** Leo on the release script.

**Blockers**

- **I'm blocked on** the design for the settings page.
- **I'm waiting for** a review from the security team.
- **No blockers** for me.

**Keeping it short**

- **Let's take this offline.**
- **I can give more details after the standup.**

## Common mistakes

**"Yesterday I have fixed the bug."**
With a finished time like *yesterday*, use the past simple, not the present perfect: *"Yesterday I **fixed** the bug."*

**"Today I will to write the tests."**
After *will*, use the base verb without *to*: *"Today I **will write** the tests."*

**"I am blocking on the API keys."**
*I'm blocking* means you are stopping someone else. You want the passive: *"I'm **blocked** on the API keys."*

**"Yesterday I was working on the ticket, today I am working on the ticket."**
This sounds like no progress. Name the result: *"Yesterday I **finished the backend part** of the ticket. Today I'm **starting the UI**."*

## Formal vs. casual

- **Written async standup for a large team or a manager:** "Yesterday: completed the password reset flow (PR #212). Today: addressing review comments, then starting the email templates. Blockers: none."
- **Spoken in a small team:** "Finished password reset yesterday, PR's up. Today, review comments, then the email templates. All good, no blockers."

## Exercise

Write your standup update for tomorrow morning: yesterday, today and blockers. Keep it under 60 words.

Then say it out loud and time yourself. Aim for 30 seconds or less.

*Hint:* check each verb. Is "yesterday" in the past simple and "today" in *going to* or the present continuous?

## Recap

- Use yesterday, today and blockers.
- Past simple for yesterday, *going to* or present continuous for today.
- Talk about results, not activity.
- Say *I'm blocked on…*, not *I'm blocking on…*
- Take long discussions offline.
