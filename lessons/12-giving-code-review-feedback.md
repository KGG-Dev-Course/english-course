---
title: Giving Code Review Feedback
summary: Write code review comments that are clear, kind and easy to act on.
date: 2026-10-08
---

## Why this matters

Code review is where developers talk about each other's work in writing, every day. A good comment improves the code and teaches something. A badly worded one can feel like a personal attack, even when you only meant to be brief. The words you choose decide which one it is.

## The core skill

### Comment on the code, not the person

Use *this code*, *this function* or *we* instead of *you*. It keeps the focus on the work.

- About the person: *You forgot to handle the error.*
- About the code: *This call doesn't handle the error case. What happens if the API is down?*

### Say what, why and a suggestion

A useful comment explains the problem, why it matters and what to do.

```text
This query runs inside the loop, so we make one database call per user.
With 1,000 users, that's 1,000 queries. Could we load all users in one
query before the loop?
```

The reason is the most important part. Without it, the author has to guess, or they make the change without learning anything.

### Show how important a comment is

Not every comment blocks the merge. Tell the author which comments are required and which are optional. Many teams use short labels:

```text
nit: this variable could be called `retryCount` for clarity.
suggestion: we could use the existing `formatDate` helper here.
question: why do we need the timeout to be 60 seconds?
blocking: this exposes the API key in the client bundle.
```

*Nit* comes from *nitpick*: a very small, unimportant detail. Marking something as a nit tells the author, "Change it if you like, it's not a big deal."

### Ask questions

A question is often better than a statement, because you might be missing context. It also invites the author to explain.

```text
Is there a reason we're not using the cache here?
What happens if `items` is empty?
```

### Say what's good

When you see something good, say it. It's motivating, and it tells the author what to keep doing.

```text
Nice, this is much easier to read than the old version.
Great test coverage on the edge cases!
```

## Useful phrases

**Suggesting**

- **What do you think about** extracting this into a function?
- **Could we** reuse the validator from the signup form?
- **Consider** using a constant here.
- **An alternative would be to** return early.

**Explaining the problem**

- **This might cause** a race condition if two requests arrive together.
- **I think this will break** when the list is empty.
- **This is hard to follow** because of the nested ifs.

**Showing priority**

- **Non-blocking**, but…
- **Not a big deal, but** the naming is a bit inconsistent.
- **This needs to be fixed before** we merge.

**Approving**

- **Looks good to me!** (*LGTM*)
- **Approved with a few small comments.**
- **Ship it!**

## Common mistakes

**"Why you didn't use the helper?"**
In questions, put *did* before the subject: *"Why **didn't you** use the helper?"* Better still, make it about the code: *"Could we use the helper here?"*

**"This is wrong."**
Short comments like this sound harsh and don't help. Explain: *"**This returns the wrong total when a discount is applied, because it's subtracted twice.**"*

**"Change the name of variable."**
You need an article before *variable*: *"Change the name of **the** variable."*

**"Please fix it ASAP!!"**
For most comments, this sounds aggressive. If it's urgent, give the reason: *"**This needs a fix before the release tomorrow, because it breaks login on Safari.**"*

## Formal vs. casual

- **Open-source project, contributor you don't know:** "Thanks for the PR! One concern: this changes the public API, so it could break existing users. Would you be open to adding a new option instead of changing the default?"
- **Teammate you work with every day:** "nit: could rename `d` to `date`? Otherwise LGTM"

## Exercise

Choose a pull request you reviewed recently, or open one from an open-source project you use. Write three review comments:

1. One blocking issue with what, why and a suggestion.
2. One optional nit, labeled clearly.
3. One positive comment.

*Hint:* read each comment as if it was about your own code. Would you feel helped or criticized?

## Recap

- Comment on the code, not the person.
- Explain what, why and give a suggestion.
- Label priority: *nit, suggestion, question, blocking*.
- Ask questions when you might be missing context.
- Say what's good, too.
