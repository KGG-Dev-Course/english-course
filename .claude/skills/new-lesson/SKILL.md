---
name: new-lesson
description: Write the next daily lesson of the English for Software Developers course and commit it. Use when asked to create, write or add a lesson.
---

# Write the next lesson

Optional argument: a lesson number (e.g. `/new-lesson 05`). Without one, write the next lesson.

1. **Find the lesson.** List `lessons/`. The next number is one more than the highest `NN-` prefix, unless a number was given. If that lesson already exists, stop and ask before overwriting it.
2. **Read the rules.** Read `PROMPT.md`. It holds the curriculum, file layout, lesson format and writing rules. Follow it exactly. Use today's date for `date:`.
3. **Read earlier lessons.** Skim the previous 2–3 lessons so you build on them and don't re-teach.
4. **Write the file.** Create `lessons/NN-slug.md`.
5. **Check the English.** Reread every example sentence. Each "wrong" example must contain exactly the one mistake it is meant to show, and every "right" example must be natural, correct English.
6. **Check the format.** The frontmatter has `title`, `summary` and `date`. The body has no `#` heading, no HTML, no tables and no emojis.
7. **Commit.** Use `git add lessons` and commit with the message `Add lesson NN: <Title>`. Do not push. Tell the user the lesson is ready and that `git push` will publish it to the blog.
