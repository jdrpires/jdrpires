# Palavras que Encantam · No Divã Treinamentos

**Cultural Technology · Digital Operations · Security · Auditability**

| | |
|---|---|
| **Role** | Architecture · Engineering leadership · Delivery |
| **Domain** | Cultural initiative · Registration · Evaluation · Operations |
| **Architecture** | Web platform + PostgreSQL + secure document workflow + role-based backoffice |
| **Core themes** | Integrity, traceability, idempotency, RLS, file security, operational governance |
| **Lifecycle** | Production |
| **Repository** | Private / client operation |

## Context

**Palavras que Encantam**, an initiative of No Divã Treinamentos, required more than an online registration form. The operation needed to receive submissions, preserve documents and participant data, generate reliable protocols, coordinate administrative work and support human evaluation by jurors.

The result became a useful case of how software architecture can support the **execution and governance of a cultural initiative using cultural-incentive mechanisms**, without confusing the technology layer with legal or regulatory compliance itself.

## The operational challenge

A cultural program can look simple from the outside: publish a call, receive entries and select submissions. Operationally, that becomes a chain of responsibilities and evidence.

The platform therefore needed to address:

- a structured participant journey;
- integrity across multiple registration stages;
- safe handling of uploaded material;
- deterministic protocol generation;
- controlled administrative access;
- juror invitation and evaluation workflows;
- separation of roles and data access;
- traceability of operational actions;
- production reliability during the submission window.

## Architecture

```text
Participants
     │
     ▼
Six-step Registration
     │
     ├── Validation / Idempotency
     ├── Secure File Handling
     ├── Anti-abuse Controls
     └── Protocol Generation
     │
     ▼
PostgreSQL / Row-Level Security
     │
     ├──────────────┐
     ▼              ▼
Administration   Jury Workflow
     │              │
     └──────┬───────┘
            ▼
   Traceable Operation
```

## Operational scale

The first production cycle has already supported:

- **116+ registrations**;
- a **six-stage** submission journey;
- administrative and juror backoffice experiences;
- document upload and security controls;
- protocol-based submission identification;
- controlled invitation/access workflows;
- role-aware database access through RLS.

These numbers describe the operating case at this stage; they are not presented as a guarantee of future scale.

## Engineering decisions

### Integrity before convenience

Multi-step operations were designed around deterministic progress, validation and idempotency rather than relying only on browser state.

### Uploaded files are an attack surface

The document workflow includes validation, quarantine/antivirus controls and operational handling designed around the assumption that public uploads are untrusted.

### Authorization belongs below the UI

Role separation is reinforced at the data layer through Row-Level Security instead of depending exclusively on frontend visibility.

### Human evaluation remains human

The platform structures access, distribution and operational traceability for jurors while keeping the evaluation decision with the people responsible for it.

### Operations need evidence

Protocols, controlled actions and traceable workflows make it possible to understand what happened during the process instead of treating the application as a disposable form.

## Stack

`Next.js` · `PostgreSQL` · `Supabase` · `Vercel` · `Linux` · `RLS` · `ClamAV` · `Turnstile` · `Security` · `Workflow Automation`

## My contribution

I worked on solution architecture, security, operational workflows and production delivery, connecting engineering decisions to the realities of the cultural operation.

The central architectural goal was to turn a public submission process into a **reliable operating system for the initiative**, rather than a collection of forms and manual controls.

## Why this became a relevant case

Palavras que Encantam demonstrates a broader pattern: projects supported by cultural-incentive mechanisms can benefit from the same engineering disciplines expected in other serious digital operations — identity, authorization, security, data integrity, traceability and operational visibility.

Technology does not replace the legal, accounting or cultural-governance responsibilities of an incentivized project. It can, however, provide a much stronger operational foundation for executing those responsibilities.

## Engineering outcome

The project evolved from a registration requirement into a **secure and traceable digital operation connecting participants, administrators, documents and jurors in one controlled workflow**.

> **Confidentiality:** participant data, credentials, private client information and implementation details that could weaken security are intentionally excluded.

[← Portfolio index](README.md)
