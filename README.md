# MD. Riajuddin Rumman

> Full-stack **Node.js** developer — Next.js and React on the client, Express and NestJS on the server — who likes the hard part of an API more than the demo: concurrency invariants, auth that fails safely, realtime channels, and tests that prove it. DevOps practice is next on the list, AI-assisted features after that.

- Building **NestJS services** on Postgres, with Prisma and TypeORM, Redis for cache and queues
- Serving the same domain over **REST, WebSockets, and GraphQL** — REST documented through Swagger
- Enforcing correctness **in the database**, not only in application code
- Solving **2–3 LeetCode problems daily** — hashing and arrays first, then graphs and DP
- Reading **system design**: idempotency, locking, exclusion constraints, where caching actually pays
- Learning the delivery side in public — **Docker, AWS, CI/CD**

<br>

## Flagship project — ShebaBook API

A service-booking backend where customers request appointments with local providers, and the system **refuses anything that would double-book someone**. Built as a portfolio piece for backend roles, so the emphasis is on rules that are correct and tested rather than the number of endpoints.

[![NestJS](https://img.shields.io/badge/NestJS-E8E8E3?style=flat-square&logo=nestjs&logoColor=E94E5B)](https://nestjs.com)
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)](https://prisma.io)
[![PostgreSQL](https://img.shields.io/badge/Postgres-336791?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![Vitest](https://img.shields.io/badge/Tests-154%20passing-00B87B?style=flat-square&logo=vitest&logoColor=white)](https://vitest.dev)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com)

- **Overlap prevention that survives races** — slot conflicts are checked in a pure `overlap` module *and* locked down by hand-written constraints in the migration SQL, so a bad request loses even under concurrent writes
- **Auth without shortcuts** — `scrypt` password hashing, JWT sign/verify that rejects malformed claims, role guards returning 401 vs 403 deliberately, and timing equalization on login
- **Layering** — `auth`, `bookings`, and `prisma` as Nest modules with DTOs separated, `current-user` data read only off the request
- **A real test pyramid** — 113 unit tests with no database required, plus 41 end-to-end tests against Postgres that create their own schema
- **Reproducible setup** — `npm ci` → `prisma generate` → `docker compose up -d` (or any reachable Postgres 14+), then `prisma migrate dev`

Repo: **[RiajuddinRumman/ShebaBook](https://github.com/RiajuddinRumman/ShebaBook)**

<br>

## Also shipping — NestJS security & realtime foundation

A framework layer I keep refining alongside the booking API, wiring the parts every production service eventually needs:

- **Realtime** — `@nestjs/websockets` on `@nestjs/platform-socket.io`, so Socket.IO gateways sit inside the same DI container as the REST controllers
- **Auth surface** — Passport with JWT strategy, JWKS key verification, Argon2 hashing, and CSRF protection on top of `helmet`
- **Throughput safety** — `@nestjs/throttler` backed by Redis for rate limiting, and `@nestjs/bull` for background jobs that must not block a request
- **Persistence both ways** — TypeORM with scripted migrations and seeders, and Zod plus `class-validator` for request contracts
- **Documented by default** — `@nestjs/swagger` generating the OpenAPI spec from the decorators, plus file uploads via Multer and delivery via Nodemailer

Repo: **[Advance-Webtech-Fall-26-27](https://github.com/RiajuddinRumman/Advance-Webtech-Fall-26-27)**

<br>

## Stack

**Frontend**

<img src="https://skillicons.dev/icons?i=react,nextjs,tailwind,js,html,css&theme=dark" alt="Frontend stack" />

**Backend & data**

<img src="https://skillicons.dev/icons?i=nodejs,express,nestjs,ts,prisma,postgres,redis&theme=dark" alt="Backend and data stack" />

**API surfaces**

![REST](https://img.shields.io/badge/REST%20_%20Swagger-FFA42C?style=flat-square&logo=nestjs&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket%20_%20Socket.IO-01C9AA?style=flat-square)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square)
![Queues](https://img.shields.io/badge/Queues%20_%20Bull%20%2B%20Redis-CB3837?style=flat-square)

**Delivery — learning in public**

<img src="https://skillicons.dev/icons?i=git,docker,aws,githubactions&theme=dark" alt="DevOps tooling" />

<br>

## Where I stand

<table>
  <tr>
    <td width="50%">

###### Built and verifiable

- **NestJS architecture** — modules, guards, interceptors, DTO validation, layered error taxonomy
- **Data integrity** — Prisma and TypeORM schemas as source of truth, versioned migrations, seeders
- **Testing strategy** — pure units beside framework-coupled e2e; supertest over HTTP; coverage scripts
- **CS fundamentals** — OOP coursework across Python, Java, and C#

    </td>
    <td width="50%">

###### Deliberately next

- **Public Next.js apps** — the client work is real; the repositories are what I owe it
- **Containers** — running the Compose stack the repos document, then images of my own
- **CI/CD** — checks on every pull request, then gated promotion to production
- **AWS** — moving containerized services onto managed compute and storage
- **AI integration** — embeddings, vector search, and streamed LLM responses inside real apps

    </td>
  </tr>
</table>

<br>

## Daily coding practice

Consistency beats intensity. I solve in **C++** and keep the practice on LeetCode rather than in a repo — the card below is a public record of where the habit stands, not a highlight reel. It's also what feeds my system-design instinct: the structures that make an algorithm fast are the same ones that keep a service correct under load.

<a href="https://leetcode.com/u/riajuddinrumman/">
  <img src="https://leetcard.jacoblin.cool/riajuddinrumman?theme=light,dark&ext=activity" alt="LeetCode stats and activity graph" />
</a>

<br>

## GitHub metrics

<table>
  <tr>
    <td>
      <img src="https://github-readme-stats.vercel.app/api?username=RiajuddinRumman&theme=transparent&hide_border=true&show_icons=true&rank_rank=true&count_private=true" alt="GitHub stats" />
    </td>
    <td>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=RiajuddinRumman&theme=transparent&hide_border=true&layout=compact&langs_count=8" alt="Top languages" />
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <img src="https://streak-stats.demolab.com/?user=RiajuddinRumman&theme=transparent&hide_border=true" alt="Contribution streak" />
    </td>
  </tr>
</table>

<br>

## Let's connect

**Open to full-stack and backend engineering internships** — ShebaBook above is the work I'd point at first.

Happy to compare notes on NestJS architecture, database constraints as a correctness tool, interview prep, or system design tradeoffs.

[![Email](https://img.shields.io/badge/Email-mdriajuddinrumman@gmail.com-0A66C2?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mdriajuddinrumman@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/md-riajuddin-rumman-50550b28a/)
[![LeetCode](https://img.shields.io/badge/LeetCode-Daily%20Solver-FF9D05?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/riajuddinrumman/)
[![GitHub](https://img.shields.io/badge/GitHub-RiajuddinRumman-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RiajuddinRumman)
