---
title: Writing Clear Slack and Chat Messages
summary: Write chat messages that people understand on the first read and can answer quickly.
date: 2026-10-06
---

## Why this matters

Most developers spend hours every day in Slack, Teams or Discord. A clear message gets a fast answer. An unclear one starts a long back-and-forth, and in a team across time zones, each question can cost a whole day.

## The core skill

### Don't just say "hi"

Many people write "Hi" and then wait for an answer before asking their question. The other person sees a notification, stops working, and then has to wait too. Put the greeting and the question in the same message.

```text
Hi Marco! Quick question about the deploy script: does it run the
database migrations, or do I need to run them by hand?
```

### Put the main point first

Busy people read the first line and decide whether to read the rest. Start with what you need, then give the details.

```text
Can someone review my PR today? It fixes the broken signup emails.
https://github.com/acme/web/pull/482
It's small (about 40 lines), mostly in mailer.ts.
```

Compare this with a message that starts with a long story and asks the question in the last line. The reader has to search for the point.

### One message, not five

Write your full thought, then press Enter. Five short messages mean five notifications.

```text
Hey
So
I was looking at the logs
and there's a lot of 500 errors
since the deploy
```

Write it as one message instead:

```text
Hey, I'm seeing a lot of 500 errors in the logs since this morning's deploy.
Is anyone else looking at this?
```

### Make it easy to answer

Give people everything they need: links, error messages, versions, and a clear question. A yes/no question or a choice is the easiest to answer.

```text
@Lena the staging DB is full again. Should I delete the old test data,
or would you prefer to increase the disk size?
```

Use threads for replies, so the main channel stays readable. Use code formatting for code, commands and errors.

## Useful phrases

**Opening**

- **Quick question about** the release process:
- **Heads-up:** the API will be down for 10 minutes at 3pm. (*heads-up* = a warning about something that will happen)
- **FYI**, I merged the new config. (*FYI* = for your information)

**Asking**

- **Does anyone know** why the build is so slow today?
- **Who's the best person to ask about** the billing service?
- **Could you take a look at** this when you have a minute?

**Following up**

- **Any update on** this?
- **Just bumping this** in case it got lost. (*bump* = bring a message back to the top)
- **Thanks, that fixed it!**

**Closing a conversation**

- **Got it**, thanks!
- **Sounds good.**
- **No worries**, I'll figure it out.

## Common mistakes

**"Please do the needful."**
This phrase is common in some countries but sounds strange to many English speakers. Say exactly what you need: *"Could you **restart the staging server**, please?"*

**"I have a doubt about the API."**
In standard English, *a doubt* means you think something may be false. For a question, say: *"I have a **question** about the API."*

**"Can you check?"**
Without context, the reader doesn't know what to check or why. Give details: *"Can you check **why the nightly build failed? Here's the log:** …"*

**"Hi, are you there?"**
This forces the other person to answer before they know what you need. Ask directly: *"Hi, **are you free to pair on the cache bug** this afternoon?"*

## Formal vs. casual

- **To a large company channel or another team:** "Hi everyone, the payments API will be unavailable on Saturday from 2:00 to 3:00 UTC for maintenance. Please let us know in this thread if this affects your team."
- **To your own team:** "Heads-up: payments API down Sat 2–3 UTC for maintenance."
- **To one close teammate:** "btw I'm taking the API down Sat for an hour, just so you know"

Abbreviations like *btw* (by the way) and lowercase writing are fine with close teammates, but avoid them with managers, clients or people you don't know.

## Exercise

Find the last three questions you asked in chat at work. Rewrite each one so that:

1. The greeting and question are in one message.
2. The main point is in the first line.
3. It includes a link, error or other detail the reader needs.

*Hint:* read your new message as if you knew nothing about the problem. Could you answer it without asking anything back?

## Recap

- Never send just "hi". Put the question in the same message.
- Put the main point in the first line.
- Write one complete message, not many small ones.
- Include links, errors and a clear question.
- Say *question*, not *doubt*, when you want to ask something.
