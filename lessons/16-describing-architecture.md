---
title: Describing Architecture and Systems
summary: Describe how a system's parts connect and how data flows through it, in clear spoken or written English.
date: 2026-10-08
---

## Why this matters

Sooner or later, someone will ask you, "How does this system work?" A new teammate, an architect, an interviewer or another team needs a clear picture. Describing architecture well helps teams make good decisions, and it's a key skill in system design interviews.

## The core skill

### From big to small

Start with the big picture, then go into the parts. Don't start with the database schema.

```text
At a high level, we have a web app, an API and a few background workers.
The web app talks to the API, and the API stores data in PostgreSQL.
Slow tasks, like sending emails, go to a queue, and the workers
process them.
```

*At a high level* means "without the details". It's a very common phrase for starting an architecture explanation.

### Follow the data

The easiest way to explain a system is to follow one request from start to finish. Use sequence words: *first, then, after that, finally.*

```text
When a user places an order, the web app first sends it to the API.
The API then checks the stock and saves the order.
After that, it publishes an "order created" event.
Finally, the email worker receives the event and sends the confirmation.
```

### Verbs for connections

Choose specific verbs to show how components relate:

- The frontend **calls** the API.
- The API **reads from** and **writes to** the database.
- The service **publishes** events **to** Kafka, and the worker **consumes** them.
- The gateway **sits in front of** all the services.
- Requests **go through** the load balancer.
- The billing service **depends on** the user service.

### Explaining why

Architecture is about decisions. Explain why a part exists, and what problem it solves.

```text
We put Redis in front of the database because the product pages get
a lot of traffic, and most of the data doesn't change often.
We split notifications into a separate service so that a problem with
email doesn't affect checkout.
```

*So that* introduces a purpose: *We did X so that Y happens.*

## Useful phrases

**Overview**

- **At a high level,** the system has three parts.
- **The main components are** the API, the queue and the workers.
- **It's a monolith**, but we're **moving to** microservices.

**Data flow**

- **The request comes in through** the API gateway.
- **The data is stored in** S3.
- **The result is sent back to** the client.
- **It runs asynchronously**, in the background.

**Reasons and trade-offs**

- **We chose** PostgreSQL **because** we need transactions.
- **The trade-off is that** it's harder to debug.
- **This allows us to** scale each service separately.

**Problems and limits**

- **The bottleneck is** the database. (*bottleneck* = the slowest part, which limits everything else)
- **It's a single point of failure.** (if it fails, everything fails)
- **It doesn't scale well** beyond a million users.

## Common mistakes

**"The frontend sends request to the API."**
*Request* is countable, so you need an article: *"The frontend sends **a** request to the API."*

**"The data is saving in the database."**
For something that is done to the data, use the passive, *is* + past participle: *"The data **is saved** in the database."*

**"The worker depends of the queue."**
The preposition is *on*: *"The worker depends **on** the queue."*

**"We use Redis for cache the sessions."**
For purpose, use *to* + verb: *"We use Redis **to cache** the sessions."*

## Formal vs. casual

- **Design document or interview:** "The system follows an event-driven architecture. The order service publishes events to Kafka, and downstream services, such as billing and notifications, consume them independently."
- **Explaining to a new teammate at a whiteboard:** "So orders come in here, get saved, and then we fire an event. Billing and emails both listen for it and do their thing."

*Do their thing* is a casual way to say "do their normal job".

## Exercise

Choose a system you work on. Describe it in two parts:

1. **Overview** (3–4 sentences): the main components and how they connect.
2. **One request** (4–5 sentences): follow one user action from start to finish, using *first, then, after that, finally*.

Then add one sentence explaining why one part of the design exists.

*Hint:* draw a simple box diagram first, then describe it out loud as if you were in an interview.

## Recap

- Start at a high level, then go into details.
- Follow one request through the system.
- Use specific verbs: *calls, publishes, consumes, depends on*.
- Explain why each part exists, using *because* and *so that*.
- Use *to* + verb for purpose: *We use Redis to cache sessions.*
