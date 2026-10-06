# Lesson Rules

The curriculum and writing rules for this course. In Claude Code, run `/new-lesson` and it follows this file. With another AI, copy everything below the line and fill in **Today**.

---

You are writing one lesson of "English for Software Developers", a free 30-lesson course. The lessons are published on a blog, one per day. Write today's lesson.

## Who it's for

The readers are software developers whose first language isn't English, at an intermediate (B1–B2) level. They can read technical docs but want to sound clearer and more confident at work: in messages, meetings, code reviews and job interviews.

## Today

- Lesson number: **NN** (for example 02)
- Date: **YYYY-MM-DD**

Write the lesson whose number matches the curriculum below. If earlier lessons are in `lessons/`, read them first. Build on what they taught and don't re-teach it.

## Curriculum

**Part 1: Everyday work communication**
1. Introducing Yourself as a Developer (already written)
2. Talking About What You're Working On
3. Writing Clear Slack and Chat Messages
4. Asking for Help Without Wasting Anyone's Time
5. Giving a Daily Standup Update
6. Writing Professional Emails
7. Polite Requests and Softening Language
8. Saying No and Pushing Back Politely

**Part 2: Technical English**
9. Explaining a Bug Clearly
10. Writing Good Commit Messages
11. Writing Pull Request Descriptions
12. Giving Code Review Feedback
13. Receiving Code Review Feedback
14. Explaining Technical Ideas to Non-Technical People
15. Writing Documentation and READMEs
16. Describing Architecture and Systems

**Part 3: Meetings and speaking**
17. Speaking Up in Meetings
18. Agreeing, Disagreeing and Making Suggestions
19. Asking Clarifying Questions
20. Presenting a Demo
21. Small Talk with Colleagues
22. Pronunciation of Common Tech Words

**Part 4: Career and job hunting**
23. Writing Your Resume in English
24. Writing a Cover Letter and Recruiter Messages
25. Answering "Tell Me About Yourself"
26. Behavioral Interviews and the STAR Method
27. Talking Through Code in a Technical Interview
28. Negotiating Salary and Offers
29. Common Grammar Mistakes Developers Make
30. Final Review: Your Personal Phrasebook

## File to create

`lessons/NN-short-slug.md`, for example `lessons/02-current-work.md`.
- The filename must start with the two-digit lesson number. The site uses that number to order the lessons.
- The slug may contain only lowercase letters, digits and hyphens.

Do not change `course.json`, `README.md` or any other lesson.

## Lesson format

The file must begin with this frontmatter, exactly:

```markdown
---
title: <Lesson title from the curriculum>
summary: <One sentence, under 120 characters, saying what the reader can do after this lesson>
date: <YYYY-MM-DD>
---
```

Then write the body in this order, using `##` headings. Never use `#`, because the site renders the title itself.

1. **Why this matters**: 2–3 sentences on the real work situation where the reader needs this.
2. **The core skill**: 2–4 short subsections. Each one explains a structure or rule and shows a realistic example from developer work, such as a Slack message, an email, a PR comment or something said in a meeting.
3. **Useful phrases**: grouped bullet lists of ready-to-use phrases, with the key words in **bold**.
4. **Common mistakes**: 3–4 mistakes that non-native speakers really make. For each, show the wrong sentence, the corrected sentence, and a one-line explanation.
5. **Formal vs. casual** (when relevant): the same message written for different situations.
6. **Exercise**: one writing or speaking task the reader can finish in 10–15 minutes, about their own work. Add a hint. Do not include a model answer.
7. **Recap**: 3–5 bullet points.

## Writing rules

- Write in simple, clear English at a B1–B2 level. Explain any idiom or phrasal verb the first time you use it.
- Use short paragraphs and a friendly, direct tone. Address the reader as "you".
- Aim for 700–1,200 words. A lesson should take about 10 minutes to read.
- Every example must be realistic for a software developer. Use names, tools and situations from real teams.
- Teach grammar only when a real example needs it, and explain it in one or two plain sentences without heavy terminology.
- Put example messages, emails and dialogues in `text` code blocks, or in quotes inside bullet lists.
- Use plain Markdown only: headings, paragraphs, lists, code blocks, links, bold and italics. No HTML, tables, images or emojis, because the blog cannot render them.

## Before you finish

Check each item:
- The frontmatter is valid and the date matches today's.
- Every "correct" example is natural, correct English, and every "wrong" example contains only the mistake it demonstrates.
- No table, HTML or emoji appears anywhere.
- No topic from a later lesson is taught in depth.

Then suggest a one-line commit message, in the form `Add lesson NN: <Title>`.
