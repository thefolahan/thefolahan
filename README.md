## Omisakin Joshua

**Founder and engineer.** I design and ship complete systems — the schema, the
API, the web and mobile clients, and the pipeline that carries each release into
production. I work across the TypeScript and JVM ecosystems, and I'm most useful
on the problems that sit between the layers: data modelling, service boundaries,
and the failure modes that only appear under real traffic. Based in Lagos.

---

### How I build

**Model the domain before choosing the framework.**
The data model outlives every framework decision made around it, so it gets
designed first. Invariants live in the database as constraints and foreign keys
rather than as application-layer conventions, and the migration history stays the
single source of truth for what the schema actually is.

**One repository, one set of contracts.**
The API and its clients compile against types generated from the same source, so
a breaking change surfaces as a failed build rather than a runtime 500 in
someone's hands. Shared packages keep validation, error shapes, and domain types
identical on both sides of the wire.

**Portable by construction.**
Everything builds from a Dockerfile any host can run, with no dependency on a
provider's proprietary primitives. Infrastructure is declared as code and treated
as replaceable — changing providers should cost a `pg_dump` and a redeploy, not a
rewrite.

**Deploys that fail before users do.**
Migrations run against the exact image about to serve traffic, gated behind a
health check, so a bad migration fails the deploy instead of the request path.
Small, reversible diffs over big-bang releases; rollback is a deployment target,
not an incident.

**Security and observability are build-time concerns.**
Argon2id password hashing, short-lived tokens with rotation, rate limiting at the
edge, and structured JSON logs with request correlation — designed in from the
first commit, because retrofitting any of them means touching every handler.

---

### Working with

| | |
|---|---|
| **Languages** | TypeScript · Java · JavaScript · Python · Kotlin · Go · C# |
| **Frontend** | React · Next.js · React Native (Expo) · Tailwind CSS |
| **Backend** | NestJS · Node.js · Spring Boot · REST / OpenAPI |
| **Data** | PostgreSQL · PostGIS · Prisma · Redis |
| **Infrastructure** | Docker · GitHub Actions · Render · AWS S3 |
| **Testing** | Jest · integration tests against real Postgres |

---

### Elsewhere

[![Email](https://img.shields.io/badge/Email-4A5568?style=flat-square&logo=gmail&logoColor=white)](mailto:officialjoshua9@gmail.com)
[![X](https://img.shields.io/badge/X-4A5568?style=flat-square&logo=x&logoColor=white)](https://x.com/thefolahan)

<sub>Available for founding-engineer and technical-lead roles, and for consulting on systems that need to ship quickly and stay standing once they're live.</sub>
