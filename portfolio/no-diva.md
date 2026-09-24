# No Divã Treinamentos

**Digital Platform · Workflow Automation · Security · Backoffice**

| | |
|---|---|
| **Role** | Architecture · Engineering leadership · Delivery |
| **Domain** | Registration, evaluation and administrative workflows |
| **Architecture** | Web app + PostgreSQL + secure document workflow + backoffice |
| **Core themes** | Integrity, idempotency, RLS, file security, auditability |
| **Lifecycle** | Production |
| **Repository** | Private / client operation |

## Context

No Divã Treinamentos required a production platform capable of supporting a structured public-facing process with registration, document handling, administrative operations and human evaluation workflows.

## Challenge

The challenge was not simply creating a form. The platform needed to preserve data integrity across a multi-step journey, safely process uploaded material, support multiple operational roles and maintain traceability throughout the process.

## Architecture

```text
Public Registration
       │
       ▼
 Multi-step Workflow
       │
       ├── Validation / Idempotency
       ├── File Security / Quarantine
       └── Protocol Generation
       │
       ▼
   PostgreSQL / RLS
       │
       ▼
Role-based Backoffice
 Admin · Jury · Operations
```

## Engineering decisions

- Multi-step registration with deterministic progress.
- Idempotent operations and unique protocol generation.
- Secure file handling with validation/quarantine controls.
- Role-specific backoffice experiences.
- Invitation and controlled-access workflows.
- Database-level access policies through RLS.
- Rate limiting and anti-abuse measures.
- Auditable evaluation and administrative actions.
- Production deployment, backups and operational controls.

## Stack

`Next.js` · `PostgreSQL` · `Supabase` · `Vercel` · `Linux` · `RLS` · `Security` · `Workflow Automation`

## My contribution

I worked on the solution architecture, security model, operational workflows and production delivery, with emphasis on making the system reliable enough to support a real process rather than treating it as a one-off website.

## Engineering outcome

The project transformed a seemingly conventional registration flow into an **operational system with security, traceability and controlled decision workflows**.

> **Confidentiality:** participant data, credentials and client-specific implementation details are intentionally excluded.

[← Portfolio index](README.md)
