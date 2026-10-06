# English for Software Developers

A daily English course for developers: write clearer messages, speak up in meetings and pass interviews. A new lesson is added every day.

## Structure

```
course.json   Course title, description and planned lesson count
lessons/      One markdown file per lesson (01-intro.md, 02-...)
PROMPT.md     Curriculum and writing rules
```

## Adding a lesson

With Claude Code, run `/new-lesson`. To write one by hand, create `lessons/NN-topic.md` with this frontmatter:

```markdown
---
title: Lesson title
summary: One-line summary
date: YYYY-MM-DD
---
```

Then commit and push. The number at the start of the filename sets the lesson order.
