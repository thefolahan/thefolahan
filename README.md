## Omisakin Joshua

**Founder and engineer.** I design and ship complete systems: the schema, the
API, the web and mobile clients, and the pipeline that carries each release into
production. I work across the TypeScript and JVM ecosystems, and I am most useful
on the problems that sit between the layers, such as data modelling, service
boundaries, and the failure modes that only appear under real traffic. Based in
Lagos.

***

### How I build

**Model the domain before choosing the framework.**
The data model outlives every framework decision made around it, so it gets
designed first. Invariants live in the database as constraints and foreign keys
rather than as application layer conventions, and the migration history remains
the single source of truth for what the schema actually is.

**One repository, one set of contracts.**
The API and its clients compile against types generated from the same source, so
a breaking change surfaces as a failed build rather than as a runtime error in
somebody's hands. Shared packages keep validation rules, error shapes, and domain
types identical on both sides of the wire.

**Portable by construction.**
Everything builds from a Dockerfile that any host can run, with no dependency on
a single provider's proprietary primitives. Infrastructure is declared as code
and treated as replaceable, so moving between providers should cost a `pg_dump`
and a redeploy rather than a rewrite.

**Deploys that fail before users do.**
Migrations run against the exact image that is about to serve traffic, gated
behind a health check, so a failed migration stops the deployment instead of
reaching the request path. Small, reversible changes are preferred over large
releases, and rollback is a deployment target rather than an incident.

**Security and observability belong in the first commit.**
Argon2id password hashing, access tokens with a short lifetime and rotation,
rate limiting at the edge, and structured JSON logs carrying a request
correlation identifier are all designed in from the beginning, because
retrofitting any one of them means revisiting every handler.

***

### Working with

* **Languages:** TypeScript, Java, JavaScript, Python, Kotlin, Go, C#
* **Frontend:** React, Next.js, React Native (Expo), Tailwind CSS
* **Backend:** NestJS, Node.js, Spring Boot, REST and OpenAPI
* **Data:** PostgreSQL, PostGIS, Prisma, Redis
* **Infrastructure:** Docker, GitHub Actions, Render, AWS S3
* **Testing:** Jest, integration tests against a real PostgreSQL instance

***

### Elsewhere

[![Email](https://img.shields.io/badge/Email-4A5568?style=flat-square&logo=gmail&logoColor=white)](mailto:officialjoshua9@gmail.com)
[![X](https://img.shields.io/badge/X-4A5568?style=flat-square&logo=x&logoColor=white)](https://x.com/thefolahan)

<sub>Available for founding engineer and technical lead roles, and for consulting on systems that need to ship quickly and stay standing once they are live.</sub>
