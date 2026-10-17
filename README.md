# MD. Riajuddin Rumman

> Computer Science undergraduate and backend-focused **Node.js** developer who likes the hard part of an API more than the demo — concurrency invariants, auth that fails safely, and tests that prove it. NestJS and TypeScript today; React/Next.js, DevOps, and AI-assisted features next.

- Writing **NestJS services with Prisma + Postgres**, validated DTOs, and a global `ValidationPipe`
- Enforcing correctness **in the database**, not only in application code
- Solving **2–3 LeetCode problems daily** — hashing and arrays first, then graphs and DP
- Reading **system design**: idempotency, locking, exclusion constraints, and where caching actually pays
- Keeping setup reproducible — one lockfile, migrations in version control, and lint, typecheck, and tests as gates

<br>

## Flagship project — ShebaBook API

A service-booking backend where customers request appointments with local providers, and the system **refuses anything that would double-book someone**. Built as a portfolio piece for backend roles, so the emphasis is on rules that are correct and tested rather than the number of endpoints.

[![NestJS](https://img.shields.io/badge/NestJS-E8E8E3?style=flat-square&logo=nestjs&logoColor=E94E5B)](https://nestjs.com)
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)](https://prisma.io)
[![PostgreSQL](https://img.shields.io/badge/Postgres-336791?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![Vitest](https://img.shields.io/badge/Tests-154%20passing-00B87B?style=flat-square&logo=vitest&logoColor=white)](https://vitest.dev)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com)

**What it exercises**

- **Overlap prevention that survives races** — slot conflicts are checked in a pure `overlap` module *and* locked down by hand-written constraints in the migration SQL, so a bad request loses even under concurrent writes
- **Auth without shortcuts** — `scrypt` password hashing, JWT sign/verify that rejects malformed claims, role guards returning 401 vs 403 deliberately, and timing equalization on login
- **Layering** — `auth`, `bookings`, and `prisma` as Nest modules with DTOs separated, `current-user` data read only off the request
- **A real test pyramid** — 113 unit tests with no database required, plus 41 end-to-end tests against Postgres that create their own schema
- **One lockfile, one command** — `npm ci` → `prisma generate` → `docker compose up -d` (or any reachable Postgres 14+), then `prisma migrate dev` — reproducible on a clean machine

Repo: **[RiajuddinRumman/ShebaBook](https://github.com/RiajuddinRumman/ShebaBook)**

<br>

## Stack

**Backend — where I work daily**

<img src="https://skillicons.dev/icons?i=nodejs,nestjs,express,ts,prisma,postgres&theme=dark" alt="Backend stack" />

**Frontend — actively building toward**

<img src="https://skillicons.dev/icons?i=react,nextjs,tailwind,js,html,css&theme=dark" alt="Frontend stack" />

**Tooling & delivery**

<img src="https://skillicons.dev/icons?i=git,vitest,npm,vscode&theme=dark" alt="Tooling and delivery" />

<br>

## Learning roadmap

<table>
  <tr>
    <td width="50%">

###### Solid now

- **REST API design** — resource modeling, DTO validation, error taxonomy in NestJS
- **Data integrity** — Prisma schema as single source of truth, versioned migrations
- **Testing strategy** — pure units beside framework-coupled e2e; supertest over HTTP
- **CS fundamentals** — OOP coursework across Python, Java, and C#

    </td>
    <td width="50%">

###### Deliberately next

- **React & Next.js** — server components, streaming, and ISR tradeoffs
- **Containers** — running the Compose stack the repo documents, and writing images for it
- **CI/CD** — pipeline checks on every pull request, then gated promotion to production
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

**Open to backend and API engineering internships** — ShebaBook above is the work I'd point at first.

Happy to compare notes on NestJS architecture, database constraints as a correctness tool, interview prep, or system design tradeoffs.

[![Email](https://img.shields.io/badge/Email-mdriajuddinrumman@gmail.com-0A66C2?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mdriajuddinrumman@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/md-riajuddin-rumman-50550b28a/)
[![GitHub](https://img.shields.io/badge/GitHub-RiajuddinRumman-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RiajuddinRumman)
