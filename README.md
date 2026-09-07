# Freddie Philpot

Year 12 student building software, operating Linux infrastructure and developing practical security-engineering skills through projects and a home lab.

I am interested in the points where software, infrastructure and security meet: identity, access control, trustworthy data flows, useful telemetry and systems that remain understandable when something goes wrong. I am working towards degree apprenticeships and early-career opportunities in security, infrastructure and software engineering.

## Current direction

- Building applications with explicit trust boundaries, server-side authorisation and tests for failure and misuse cases.
- Running self-hosted services to learn Linux administration, networking, DNS, access control, monitoring and troubleshooting.
- Developing a documented detection and investigation lab so that my security work shows evidence, analysis and hardening—not only tool installation.

## Selected projects

### [Glyph](https://github.com/pphilfre/glyph) — private-first technical note publishing

Glyph lets a user create or import Markdown and mathematical notes, keep drafts private, and publish selected content at a stable URL.

- The backend derives ownership from the authenticated identity and enforces it for reads, edits, publishing and deletion; clients cannot choose an owner ID or attach an arbitrary stored file.
- Public access is a separate, deliberately narrow path. Unpublishing revokes subsequent metadata and source reads, while private records and storage identifiers are not returned publicly.
- Uploaded content is checked for filename, extension, size and valid text before storage. Rendered Markdown is sanitised, raw HTML is discarded, and KaTeX runs with restricted trust and resource limits.
- Automated tests exercise anonymous requests, cross-account access attempts, forged upload parameters, publication revocation, invalid files and malicious markup.

`TypeScript` · `Next.js` · `Convex` · `Clerk` · `Vitest` · `Docker`

### [Markup](https://github.com/pphilfre/markup) — linked notes across local and remote storage

Markup is a keyboard-first workspace for Markdown, mathematical notation, diagrams and linked notes. The interesting part is the storage and synchronisation problem: browser state can be hydrated from remote data, offline changes are retained and flushed after reconnection, and the Tauri desktop target can synchronise notes with local files.

It also explores graph-based backlinks, multiple document types and rendering the same content consistently across editor, preview and shared views.

`TypeScript` · `Next.js` · `PostgreSQL/Prisma` · `Convex` · `Tauri` · `CodeMirror`

### [Waypoint](https://github.com/pphilfre/waypoint) — private application and opportunity tracking

Waypoint models companies, opportunities, applications, deadlines and next actions as linked data rather than a collection of disconnected notes. Its backend validates the authenticated WorkOS identity before accessing user records, and the project includes tests for identity spoofing, private-network URL blocking, scoring, exports and deadline logic.

`TypeScript` · `React` · `TanStack Start` · `Convex` · `WorkOS` · `Vitest`

## Security and infrastructure lab

My lab spans a local Proxmox virtualisation host and Oracle Cloud Linux systems. I use Docker Compose for services, Traefik for routing and TLS, Tailscale for private remote access, and Pi-hole for DNS filtering and local records.

It is a place to practise operating systems rather than just deploying them: managing services, tracing network and DNS problems, reading logs, limiting access and recovering from configuration failures. Monitoring work has included Wazuh, Prometheus and Grafana; my next step is to turn that infrastructure into repeatable detection and investigation exercises with clear evidence.

## Building towards practical security investigations

I am designing a small, isolated Windows/Linux detection lab using Wazuh, Sysmon where appropriate, and packet analysis with Wireshark. Controlled activity will run only against systems I own.

Each write-up will follow the same structure:

> activity → telemetry → detection → investigation → mitigation

The first planned case study is an investigation of SSH authentication failures against a Linux server: reconstructing a timeline from logs, distinguishing expected mistakes from suspicious repetition, documenting the commands and evidence used, and then testing the effect of hardening changes.

## Technical areas

| Area | Experience |
| --- | --- |
| **Security and infrastructure** | Linux, Docker and Compose, Proxmox, Oracle Cloud, Traefik, Tailscale, DNS/Pi-hole, authentication, authorisation, input validation, monitoring and logging |
| **Software engineering** | TypeScript, React, Next.js, Git, automated testing, API and data modelling |
| **Data and platforms** | PostgreSQL, Prisma, Convex, Vercel, self-hosted services |
| **Currently developing** | Wazuh, Sysmon, Wireshark, practical log analysis, Python and PowerShell scripting |

## Experience and learning

During technology work experience at Tesco Head Office, I gained exposure to software development, code review, testing and deployment workflows, IT operations and enterprise infrastructure. I also shadowed cyber-security/SOC and incident-management work; this was observation and guided learning, not responsibility for production incidents or systems.

I have completed Cisco learning courses in **Introduction to Cybersecurity**, **Endpoint Security** and **Network Defense**. I use them as foundations for practical work rather than presenting them as professional certifications.

## Links

[Portfolio](https://freddiephilpot.dev) · [LinkedIn](https://www.linkedin.com/in/freddiephilpot/) · [Email](mailto:contact@freddiephilpot.dev)
