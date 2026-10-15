# claude-skills

A Claude Code **plugin marketplace** bundling 24 skills, extracted from the
[image_generator](https://github.com/HaTranBK/image_generator) project's `.claude/skills` directory.

## Install

In Claude Code, run:

```
/plugin marketplace add HaTranBK/claude-skills
/plugin install dev-skills-pack@claude-skills
```

That adds this repo as a marketplace and installs the `dev-skills-pack` plugin, which brings all 24 skills below into your session.

To update later:

```
/plugin marketplace update claude-skills
/plugin update dev-skills-pack@claude-skills
```

## What's inside

| Skill | What it's for |
|---|---|
| `ck:backend-development` | Build backends with Node.js, Python, Go (NestJS, FastAPI, Django) — REST/GraphQL/gRPC APIs, auth, databases, microservices, security, Docker/K8s |
| `ck:brainstorm` | Brainstorm solutions with trade-off analysis — ideation, architecture decisions, technical debates, feasibility |
| `ck:chrome-devtools` | Automate browsers with Puppeteer — screenshots, performance, network monitoring, scraping, JS debugging |
| `ck:code-review` | Review code quality, verify completion claims — use before PRs or after implementing a feature |
| `ck:coding-level` | Set coding experience level for tailored explanations and output format |
| `cook` | Activate before implementing any feature, plan, or fix |
| `ck:copywriting` | Conversion copywriting formulas, headlines, email/landing-page copy, CTA optimization |
| `ck:databases` | Design schemas and write queries for MongoDB/PostgreSQL — indexes, migrations, replication, performance |
| `ck:debug` | Systematic debugging with root-cause analysis before fixes |
| `ck:docs-seeker` | Search library/framework docs via llms.txt (context7.com) |
| `fix` | Activate before fixing any bug, error, test failure, CI/CD issue, type error, lint, or log error |
| `ck:frontend-design` | Create polished frontend interfaces from designs/screenshots/videos, incl. 3D |
| `ck:frontend-development` | Build React/TypeScript frontends — Suspense, TanStack Router, MUI v7, performance |
| `ck:git` | Git operations with conventional commits, auto-split by type/scope, secret scanning |
| `ck:plan` | Plan implementations, design architectures, create technical roadmaps |
| `ck:problem-solving` | Systematic problem-solving when stuck — complexity spirals, assumption constraints |
| `prompt-engineer` | Transform rough prompts/ideas into production-ready LLM prompts |
| `ck:react-best-practices` | React/Next.js performance guidelines from Vercel Engineering |
| `ck:scout` | Fast codebase scouting via parallel agents — file discovery, context gathering |
| `ck:tanstack` | Build with TanStack Start, Form, and AI |
| `ck:test` | Run unit/integration/e2e/UI tests, coverage, build verification, visual regression |
| `ck:threejs` | Build 3D web apps with Three.js (WebGL/WebGPU) |
| `ck:ui-styling` | Style UIs with shadcn/ui (Radix UI + Tailwind) — themes, dark mode, design systems |
| `ck:ui-ux-pro-max` | UI/UX design intelligence — styles, palettes, font pairings, charts, stacks |

## Layout

```
.claude-plugin/
  plugin.json        # plugin manifest (name: claude-skills)
  marketplace.json    # marketplace manifest, lists the plugin above
skills/
  <skill-name>/
    SKILL.md
    ...
```

## Notes

- `skills/ui-styling/` carries its own `LICENSE.txt` (Apache License 2.0) from its upstream source; it is kept as-is per that license's attribution requirement.
- Several skills shell out to `$HOME/.claude/skills/<name>/scripts/...` — this is how Claude Code resolves an installed skill's own scripts at runtime, not a hardcoded path to this repo.
