---
title: GitKraken AI Credits FAQ
description: Here are the most common questions about GitKraken AI Credits
product: "GitKraken.dev"
content_type: "faq"
audience: "all"
plan_required: "all"
status: "GA"
last_verified: "2026-06"
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2026</kbd>

This page answers the most common questions about GitKraken AI Credits. For organization and role management, see [Organization Management](/gk-dev/gk-dev-organization/).

***
## Why are we switching from tokens to credits?

Credits are a single, customer-facing unit that reflects the value of the work performed. Tokens were a technical artifact that forced customers to think in model internals to predict cost. With newer AI features that vary widely in compute (agent runs, long-running operations), a credit-based view is both simpler to understand and more accurately tied to what we deliver.
---

## What exactly is a credit?

A credit is a unit of work. Its size depends on the model used, the length of the request, the complexity of the operation, and how much context the feature pulled in.
---

## How many credits equal one old token?

There is no fixed conversion. The relationship between tokens and credits depends on several factors that change by request — model, length, operation type, context size. Any single number would be misleading.
---

## Can you share the formula internally so I can explain it better?

No, and here’s why: even internally, there is no single formula. The pricing team adjusts the underlying weights as models and features evolve, so any number a rep memorized today could be wrong next month. Stick to the variability framing — it ages well.
---

## Will my usage change month-to-month?

Yes, more visibly than before. Credits track usage, and usage varies. You’ll see your credit consumption move with how you use AI features, and the type of usage.
---

## What Models are being used?

We route different operations to different models based on what’s best suited to the task.
---

## What is an individual AI credit limit?

This is the AI credit limit that is used for user specific AI actions, like composing commits, explaining changes, and other AI functions generally used by individual users.
---

## What is an Organization AI credit limit?

This is the AI credit limit that is used for non user specific AI actions, like automations. In some cases, this limit may be used to cover user actions by users that have exhausted their personal credit limit.
---

## What if I run out of AI credits mid-cycle?
If your personal credit limit runs out before your next refresh, Gitkraken will start pulling from the organization’s overall available credit limit. If that limit is exhausted, then additional credits can be purchased by your organization as credit add-ons.
---

## What are credit add-ons?
Credit add-ons are additional AI credits your organization can purchase on top of its plan allotment. They’re useful when your team consistently reaches its credit limit before the next refresh. Add-on credits are pooled into the organization’s overall available credit limit and are drawn on once the plan’s included credits are exhausted. Add-on credits can only be purchased by Owners, Admins, or Billing Contacts.
---

## Will the credit cost of a given action change later?
Yes, the cost of specific operations may be adjusted as the underlying models and features evolve.
---

## How much do credits cost.
For a breakdown of pricing for credits, please see our [Pricing page](https://www.gitkraken.com/pricing) for details.
---

## Why do features cost credits in addition to the AI model?

Some AI features have an additional cost added aside from the AI cost due to value added as part of the feature functionality 
---