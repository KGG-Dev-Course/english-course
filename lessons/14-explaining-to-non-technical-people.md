---
title: Explaining Technical Ideas to Non-Technical People
summary: Explain technical problems and decisions to managers, clients and users in simple, clear words.
date: 2026-10-08
---

## Why this matters

Product managers, designers, sales teams and clients need to understand your work to make decisions. If they don't understand you, they can't support your ideas or plan around problems. Developers who explain technical things simply are trusted, and they often become team leads.

## The core skill

### Start with the impact

Non-technical people care about results: users, money, time and risk. Start with what it means for them, then add technical details only if they ask.

- Technical first: *The service has a memory leak, so the pods get OOM-killed.*
- Impact first: *The app is crashing a few times a day, so some users lose their work. We've found the cause and the fix will be ready tomorrow.*

### Replace jargon

*Jargon* is the special vocabulary of a profession. Replace it with simple words, or explain it once.

```text
Instead of: We need to refactor the auth module.
Say: We need to reorganize the login code. It won't change anything
for users, but it will make future changes faster and safer.

Instead of: The API has high latency.
Say: The system is slow to respond. Pages take about 5 seconds to load.
```

### Use comparisons

A comparison with everyday life can make an abstract idea clear.

```text
A cache is like keeping your most-used tools on your desk instead of
in the storage room. It's faster, but you need to replace them when
they get old.

Technical debt is like a loan. A shortcut saves time now, but we pay
"interest" every time we change that code later.
```

Choose comparisons that are simple and familiar. Don't push them too far: one or two sentences is enough.

### Check understanding

Don't ask "Do you understand?" It can sound like you think they're not smart. Ask a softer question instead.

```text
Does that make sense?
Is that clear, or should I explain any part in more detail?
What questions do you have?
```

## Useful phrases

**Simplifying**

- **In simple terms,** the system can't handle so many users at once.
- **Basically,** we need to replace an old part of the system.
- **What this means for you is** that the report will be ready one week later.

**Comparing**

- **It's a bit like** a phone's contact list.
- **Think of it as** a backup copy.
- **Imagine** a library where every book has a number.

**Talking about risk and time**

- **There's a small risk that** some users will need to log in again.
- **The safest option is to** wait until the weekend.
- **It will take about** two weeks, **depending on** what we find.

**Checking**

- **Does that make sense?**
- **Let me know if** I should go into more detail.

## Common mistakes

**"We need to fix the N+1 query problem in the ORM layer."**
This is correct English, but too technical for a manager. Describe the effect: *"**One page loads very slowly because it asks the database for data hundreds of times.** We need to fix that."*

**"It's very easy, you just need to clear the cache."**
*Easy* and *just* can make someone feel stupid if it isn't easy for them. Say: *"**To fix this, please clear your browser's cache.** Here's how: …"*

**"The deploy will be done until Friday."**
Use *by* for a deadline: *"The deploy will be done **by** Friday."*

**"Do you understand?"**
Correct, but it can sound like a test. Ask: *"**Does that make sense?**"*

## Formal vs. casual

- **Email to a client:** "We found the cause of the slow reports. Our database was doing much more work than necessary. We'll release a fix on Thursday, and reports should load in under two seconds."
- **Chat with your product manager:** "Found why reports are slow, the database was doing way too much work. Fix goes out Thursday."

## Exercise

Choose a technical task from your current work, like a migration, a refactor or a performance fix. Explain it in 4–5 sentences to someone in sales or marketing. Include:

1. The impact on users or the business.
2. One comparison from everyday life.
3. How long it will take, or what you need from them.

*Hint:* ask a friend or family member who doesn't work in tech to read it. Note every word they ask about.

## Recap

- Start with the impact, not the technology.
- Replace jargon, or explain it once.
- Use short, familiar comparisons.
- Avoid *easy* and *just* when someone is struggling.
- Ask *Does that make sense?* instead of *Do you understand?*
