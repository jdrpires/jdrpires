# No Divã Treinamentos

**Digital Platform · Workflow Automation · Security · Backoffice**

## Context

No Divã Treinamentos required a production platform capable of supporting a structured public-facing process with registration, document handling, administrative operations and human evaluation workflows.

## Problem space

The challenge was not simply creating a form. The platform needed to preserve data integrity across a multi-step journey, handle uploaded material safely, support different operational roles and provide traceability throughout the process.

## Engineering approach

The solution was designed around:

- multi-step registration workflows;
- idempotent operations and protocol generation;
- secure file handling and quarantine/validation flows;
- role-based backoffice experiences;
- invitation and access workflows;
- database-level access policies;
- rate limiting and anti-abuse controls;
- auditable evaluation and administrative operations;
- production deployment and operational backup practices.

## Technology themes

`Next.js` · `PostgreSQL` · `Supabase` · `Vercel` · `Linux` · `Security` · `RLS` · `Workflow Automation`

## Engineering value

This project is a useful example of turning what initially appears to be a conventional web workflow into a reliable operational system. The engineering emphasis was on correctness, security, traceability and maintainability rather than only interface delivery.

## Portfolio note

The production repository is private because it supports a real client operation. This case study excludes participant information, credentials and client-sensitive implementation details.
