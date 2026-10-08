---
title: Receiving Code Review Feedback
summary: Reply to review comments professionally, whether you agree, disagree or need more information.
date: 2026-10-08
---

## Why this matters

When you open a pull request, you'll get comments: some helpful, some confusing, some you disagree with. How you reply affects how fast your PR gets merged and how people see you. Calm, clear replies make you look confident and easy to work with.

## The core skill

### Thank and confirm

When you agree with a comment, a short reply is enough. Tell the reviewer you made the change, so they don't need to check.

```text
Good catch, thanks! Fixed in a3f9c21.
Done. I've renamed it to `retryCount`.
```

*Good catch* means "you found a real problem". It's a friendly way to thank a reviewer.

### Ask when you don't understand

Never guess what a reviewer meant. Ask a specific question.

```text
I'm not sure I understand. Do you mean we should move the validation
to the controller, or remove it completely?
Could you give an example of what you have in mind?
```

### Disagree with reasons

You don't have to accept every comment. If you disagree, explain why, using facts.

```text
I thought about using the cache here, but the data changes every few
seconds, so users would see old prices. That's why I query the database
directly. Does that make sense, or am I missing something?
```

Ending with a question keeps the discussion open and friendly. If you can't agree after two or three replies, suggest a short call. Written arguments often go in circles.

### Postpone without ignoring

Some comments are good ideas but are not part of this PR. Say so, and create a follow-up ticket.

```text
Agreed, this file needs a bigger refactor. It's out of scope for this
PR, so I've created #622 to track it.
```

A *follow-up* is a task you do later, connected to the current one.

## Useful phrases

**Agreeing**

- **Good catch**, fixed!
- **Good point.** I've updated it.
- **Makes sense**, done.
- **You're right**, I missed that case.

**Asking for clarification**

- **Just to clarify,** do you mean…?
- **Could you expand on** this a bit? (*expand on* = give more details)
- **What would you suggest instead?**

**Disagreeing**

- **I see your point, but** I chose this because…
- **I considered that, but** it would make the tests much slower.
- **I'd prefer to keep it as is**, because…
- **Happy to discuss on a call** if that's easier.

**Postponing**

- **Let's handle that in a follow-up.**
- **I've created a ticket** for it: #622.
- **I'll address that in the next PR.**

## Common mistakes

**"Ok."**
A one-word reply doesn't tell the reviewer what you did. Say: *"**Done, I've added the null check.**"*

**"I have fixed it in last commit."**
You need an article before *last commit*: *"I have fixed it in **the** last commit."*

**"No, my code is correct."**
This sounds defensive. Explain your reasons: *"**I think this is correct, because the list is always sorted before this function is called.** Let me know if I'm missing something."*

**"Thanks for your feedbacks."**
*Feedback* is uncountable. It has no plural: *"Thanks for your **feedback**."*

## Formal vs. casual

- **Reply to a maintainer on an open-source project:** "Thank you for the detailed review. I've addressed all comments except the one about the config format. I kept the current format to stay compatible with version 2. Please let me know if you'd like me to change it anyway."
- **Reply to a teammate:** "All fixed except the config one. Kept it for v2 compatibility, ok with you?"

## Exercise

Find a PR where you got comments, or imagine a reviewer wrote these three comments on your code:

1. "This function is too long."
2. "Why not use a Map instead of an object?"
3. "We should add caching here."

Write a reply to each one. Agree with one, disagree with one (with a reason), and postpone one.

*Hint:* before you write a disagreement, wait five minutes. Then check that your reply talks about the code, not about the reviewer.

## Recap

- Say *thanks* and confirm what you changed.
- Ask a specific question when a comment isn't clear.
- Disagree with reasons, and end with a question.
- Postpone good ideas with a follow-up ticket.
- *Feedback* has no plural.
