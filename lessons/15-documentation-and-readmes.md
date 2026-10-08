---
title: Writing Documentation and READMEs
summary: Write READMEs and docs that help people install, use and understand your project quickly.
date: 2026-10-08
---

## Why this matters

Good documentation answers questions before people need to ask them. A clear README saves your team hours of onboarding, and for open-source projects, it decides if people use your project or leave. Docs are also read by many non-native speakers, so simple English helps everyone.

## The core skill

### The structure of a README

Most READMEs answer these questions, in this order:

1. **What is it?** One or two sentences.
2. **How do I install it?**
3. **How do I use it?** A short example.
4. **How do I contribute or get help?**

```text
## invoice-pdf

Generates PDF invoices from JSON data. Used by the billing service.

## Installation

npm install @acme/invoice-pdf

## Usage

const pdf = await createInvoice(order);
await pdf.save("invoice.pdf");

## Running tests

npm test
```

Lead with the most useful information. Nobody wants to read the project's history before they learn how to install it.

### Instructions: use the imperative

For steps, use the imperative, like in bug reports: *Install, Run, Open, Copy.* Number the steps when the order matters.

```text
1. Copy `.env.example` to `.env`.
2. Add your API key to `.env`.
3. Run `docker compose up`.
4. Open http://localhost:3000 in your browser.
```

### Descriptions: use the present simple

To describe what the code does, use the present simple. The subject is usually the function, service or tool:

```text
This function returns the user's active subscriptions.
The worker processes jobs from the queue every 30 seconds.
If the file doesn't exist, the script creates it.
```

### Write for someone new

Write for a developer who joined the team today. Don't assume they know the internal names, tools or history.

- Assumes too much: *Run the usual setup and point it at Atlas.*
- Clear: *Run `make setup`. Then set `DB_URL` to the address of our staging database, called Atlas. You can find it in 1Password.*

Use short sentences, one idea per sentence. Avoid *simply*, *obviously* and *just*. If a step is easy for you, it may not be easy for the reader.

## Useful phrases

**Introducing**

- **This project** helps teams track deploys.
- **It's designed for** small teams that use GitHub Actions.

**Prerequisites**

- **Before you start, make sure you have** Node.js 20 installed.
- **You'll need** access to the AWS account.

**Instructions**

- **To run the tests,** use `npm test`.
- **Once that's done,** restart the server.
- **If you see** a permission error, **run** the command with `sudo`.

**Warnings and notes**

- **Note:** this only works on Linux.
- **Warning:** this command deletes all local data.
- **For more details, see** the API reference.

## Common mistakes

**"For run the project, use npm start."**
Use *to* + verb for a purpose: *"**To run** the project, use npm start."*

**"This function return a list of users."**
With a singular subject, add *-s*: *"This function **returns** a list of users."*

**"You must to set the API key."**
After *must*, use the base verb without *to*: *"You **must set** the API key."*

**"Simply configure the webhook."**
*Simply* can make the reader feel bad if they're stuck. Remove it, and add the actual steps: *"**Configure the webhook: go to Settings, then Webhooks, and add the URL.**"*

## Formal vs. casual

- **Public docs for customers:** "To authenticate, include your API key in the `Authorization` header of each request. API keys can be created in the dashboard under Settings > API."
- **Internal team notes:** "Auth: put your key in the `Authorization` header. Get one from Settings > API."

Public docs should be complete and polite. Internal notes can be shorter, but should still be clear to a new team member.

## Exercise

Choose a project you work on. Write or rewrite the first part of its README: what it is (1–2 sentences), how to install it, and how to run it locally, in numbered steps.

*Hint:* follow your steps on a clean machine, or ask a new teammate to try them. Every question they ask shows a missing step.

## Recap

- Answer: what is it, how to install, how to use, how to get help.
- Use the imperative for steps and the present simple for descriptions.
- Write for someone who joined today.
- Avoid *simply*, *obviously* and *just*.
- Use *to* + verb for purpose: *To run the tests, …*
