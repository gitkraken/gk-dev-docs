---
title: Security Information for GitKraken.dev
description: Learn how GitKraken.dev encrypts data in transit and at rest across features like Workspaces, Launchpad, and Cloud Patches.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2025</kbd>

This page outlines how GitKraken.dev handles data security—including what data we collect, how it's transmitted, where it's stored, and how it's protected at rest.


| Service | What information are we collecting | How is this information secured in the transfer| Where is this information stored | How is this information secured in storage |
| --- | --- | --- | --- | --- |
| Workspaces/Insights | Repo meta-data issues/PR’s | Encrypted with TLS | MongoDB Atlas | Encrypted at rest (AES-256) |
| Teams & Users | Repo-relative file paths, number of lines changed, name of branch currently checked out, first commit SHA of the repository | Encrypted with TLS | MongoDB Atlas | Encrypted at rest (AES-256) |
| Subscriptions | Billing info: lastFour, name, type (credit card, paypal, ach...), zip, country, creditCard type (mastercard, visa...) | Encrypted with TLS | MongoDB Atlas | Encrypted at rest (AES-256) |
| Launchpad | Storing meta-data for issues/pull-requests/URLs | Encrypted with TLS | Postgres (RDS) | Encrypted at rest (AES-256) |
| Cloud Patches | Info related to the patch (repo name/URL/provider/base branch name/etc.) + the patch content itself. | Encrypted with TLS | Patch info is stored in a Postgres database, patch content is stored in AWS S3. | SSE-S3, which uses 256-bit Advanced Encryption Standard (AES-256) |
