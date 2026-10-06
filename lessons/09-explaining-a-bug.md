---
title: Explaining a Bug Clearly
summary: Write bug reports and describe problems so others can reproduce and fix them fast.
date: 2026-10-06
---

## Why this matters

A bug that nobody can reproduce is a bug that nobody can fix. Whether you write a Jira ticket, a GitHub issue or a quick message to a teammate, a clear bug description saves hours of guessing. It's one of the most useful kinds of writing a developer does.

## The core skill

### The standard structure

Good bug reports almost always have these parts:

1. **Summary:** one line that says what's broken and where.
2. **Steps to reproduce:** numbered steps.
3. **Expected result:** what should happen.
4. **Actual result:** what really happens.
5. **Environment and details:** browser, version, logs, screenshots.

```text
Title: Checkout fails with 500 error when the cart has a discount code

Steps to reproduce:
1. Log in as a test user.
2. Add any product to the cart.
3. Apply the code SAVE10.
4. Click "Pay now".

Expected result: The order is created and the confirmation page appears.
Actual result: The page shows "Something went wrong". The API returns
500 from POST /orders.

Environment: staging, Chrome 129, build 4.12.0
Logs: "TypeError: Cannot read properties of null (reading 'amount')"
```

### Writing the steps

Use the imperative (the base verb with no subject) for each step: *Open, Click, Enter, Wait.* Keep one action per step.

```text
1. Open the Settings page.
2. Change the language to German.
3. Refresh the page.
```

### Expected vs. actual

Use the present simple for both, because you're describing general behavior:

```text
Expected: The user sees a success message.
Actual: Nothing happens, and the button stays disabled.
```

### Describing how often and since when

Developers need to know if a bug always happens. Use frequency words and *since*:

```text
It happens every time on Safari, but only sometimes on Chrome.
This started after yesterday's deploy.
It's been happening since we upgraded to React 19.
```

Also say what you already know, for example: *It doesn't happen in production* or *It only affects users with more than 100 projects.*

## Useful phrases

**Describing the problem**

- The page **crashes** / **freezes** / **hangs**. (*hang* = stop responding)
- The request **times out** after 30 seconds.
- The button **doesn't respond**.
- The data **isn't saved**.

**Frequency**

- It happens **every time** / **intermittently** (sometimes, with no clear pattern).
- I **can reproduce it consistently** on staging.
- I **can't reproduce it** locally.

**Scope**

- It **only affects** iOS users.
- It **seems to be related to** the new caching layer.
- **This is a regression**: it worked in version 4.11. (*regression* = something that worked before and is now broken)

**Severity**

- It's **blocking** all payments.
- It's **minor**, just a visual glitch. (*glitch* = small problem)
- **There's a workaround**: refreshing the page fixes it.

## Common mistakes

**"The app is not working."**
Too general. Say what part fails and how: *"**The export button returns a 404 error.**"*

**"When I click the button, the page is crashing."**
For something that happens every time, use the present simple: *"When I click the button, the page **crashes**."*

**"I can reproduce it in my computer."**
Use *on* for a device or machine: *"I can reproduce it **on** my computer."*

**"Expected: it should work."**
This tells the reader nothing new. Describe the correct behavior: *"Expected: **the file downloads as report.csv**."*

## Formal vs. casual

- **Bug ticket for another team:** "Uploading a file larger than 10 MB fails with a 413 error on staging. Steps to reproduce and logs are below. This blocks the customer import feature for the release on Oct 20."
- **Quick chat to a teammate:** "Uploads over 10 MB fail with a 413 on staging. Is that the nginx limit? Repro steps in the ticket."

*Repro* is a short, informal word for "steps to reproduce".

## Exercise

Choose a real bug you saw recently, at work or in an app you use. Write a full bug report with a summary, steps to reproduce, expected result, actual result and environment.

Then write a two-line chat message about the same bug for a teammate.

*Hint:* give your steps to someone else, or follow them yourself exactly as written. If you can't reproduce the bug, a step is missing.

## Recap

- Use a summary, steps, expected, actual and environment.
- Write steps in the imperative, one action per step.
- Use the present simple for behavior: *the page crashes*.
- Say how often it happens and since when.
- Describe the correct behavior, not just "it should work".
