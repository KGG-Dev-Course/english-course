---
title: Asking for Help Without Wasting Anyone's Time
summary: Ask technical questions that show what you tried, so people can help you quickly.
date: 2026-10-06
---

## Why this matters

Every developer gets stuck. Senior engineers are usually happy to help, but they are also busy. A well-written request for help gets a fast, useful answer and shows that you respect their time. It also makes you look more professional, not less.

## The core skill

### The four parts of a good question

A good request for help answers four questions:

1. **What are you trying to do?** The goal, not only the error.
2. **What happened?** The error message or wrong behavior.
3. **What have you tried?** So nobody suggests the same thing again.
4. **What do you need?** An answer, a review, a call, a pointer?

```text
Hi Sam, I'm trying to run the integration tests locally, but they fail
with "connection refused" on port 5432.
I've checked that Docker is running and I've restarted the postgres
container, but I get the same error.
Do you know if there's a setup step I'm missing? Happy to jump on a
quick call if that's easier.
```

The goal is important because sometimes your approach is wrong. If you only ask "how do I fix this error?", people can't tell you there's a better way.

### Show what you tried

Use the present perfect (*I've tried, I've checked*) for things you did before asking. The exact time is not important, only that you did them.

```text
I've already cleared the cache and reinstalled node_modules.
I've also searched the wiki, but I couldn't find anything about this.
```

This sentence is powerful. It tells the helper you did your homework, and it saves both of you time.

### Choose the right place

- A question many people might have: ask in the **team channel**. Others can learn from the answer.
- A question for one expert: send a **direct message**, but say why you chose them.
- Something complex: ask for a **short call** and share the details first.

```text
Hi Ana, I heard you built the original search indexer. Do you have
15 minutes this week to explain how the reindex job works?
```

### Close the loop

When the problem is solved, say so, and share the solution. *Close the loop* means to tell people the final result so nothing is left open.

```text
Update: fixed it! I was using the old .env file. Thanks for the help, Sam.
I've added a note to the setup docs.
```

## Useful phrases

**Starting**

- **I'm stuck on** the OAuth redirect.
- **I could use some help with** the deploy pipeline.
- **Sorry to bother you, but** do you know how the cron jobs are configured?

**Explaining what you tried**

- **I've already tried** restarting the service.
- **I've ruled out** a network problem. (*rule out* = decide something is not the cause)
- **It works locally, but** it fails on CI.

**Asking for a specific kind of help**

- **Could you point me in the right direction?** (= tell me where to look)
- **Is there any documentation on** this?
- **Do you have 10 minutes to** pair on it?

**Thanking**

- **Thanks, that was really helpful.**
- **I appreciate you taking the time.**

## Common mistakes

**"It doesn't work. Can you help?"**
This gives no information. Describe what you expected and what happened: *"**The login button does nothing when I click it**, and there's no error in the console. Can you help?"*

**"I tried to restart the server but it didn't work, and also I tried to clear the cache, and also I checked the logs."**
A long chain of *and also* is hard to read. Use a short list instead: *"I've tried: restarting the server, clearing the cache and checking the logs."*

**"Please help me urgently!!!"**
Too many exclamation marks sound like panic. Explain the impact instead: *"**This is blocking the release today**, so any help is appreciated."*

**"Thank you in advance for your help."**
This is fine in emails, but in chat it can sound like you expect help. *"**Thanks!**"* or *"**Any ideas?**"* is more natural.

## Formal vs. casual

- **To an engineer on another team you don't know:** "Hi Daniel, I'm a developer on the mobile team. We're getting 403 errors from the user service since yesterday. Could you tell me if anything changed with the permissions?"
- **To a teammate:** "Anyone seen this before? Getting 403s from user-service since yesterday. Already checked our tokens."

## Exercise

Think of a problem you're stuck on now, or one you had recently. Write a request for help with all four parts: your goal, what happened, what you tried and what you need.

Then write the "close the loop" message you would send after it's solved.

*Hint:* before you send a real request, give yourself 30 more minutes. Writing the "what I tried" list often helps you find the answer yourself.

## Recap

- Give your goal, the problem, what you tried and what you need.
- Use the present perfect to describe what you tried: *I've already checked…*
- Choose the right place: channel, direct message or call.
- Explain the impact instead of writing "urgent".
- Close the loop when the problem is solved.
