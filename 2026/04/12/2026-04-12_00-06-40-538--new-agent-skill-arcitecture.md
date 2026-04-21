---
id: a2a6ad72-f6e0-4d83-906c-a50c0ca21cbc
title: New Agent Skill - Arcitecture
created_at: 2026-04-12T04:06:40.540Z
datetime: 2026-04-12T04:06:40.540Z
tags: []
context: {"deviceName":"Macbook Prp","hostname":"Emmanuels-MacBook-Pro.local","activeApp":"Code","timeOfDay":"night","timestamp":"2026-04-12T04:06:40.555Z"}
---

---
name: architecture-docs
description: 'Generate or update a structured ARCHITECTURE.md for any project. Use when: starting a new project, documenting an existing codebase, onboarding a team, or keeping architecture docs in sync after major changes. Produces a 5-section document — Vision & Mission, Tech Stack Summary, File Structure, Build & Tooling, Data & Storage — with complexity ratings, annotated directory trees, and command tables.'
argument-hint: 'Optional: path to existing ARCHITECTURE.md to update, or "new" to generate from scratch'
---

# Architecture Docs

Produce a structured `ARCHITECTURE.md` that serves as the single source of truth for a project's technical structure.

## When to Use
- Starting a new project and need to document the architecture
- Onboarding team members or agents to an existing codebase
- Major refactor or feature addition that changes the structure
- Keeping docs in sync after dependency, file, or IPC changes

## Output Structure

Every ARCHITECTURE.md has exactly these 5 sections in this order:

### 1. Vision & Mission
- **One-line idea**: What the product does in plain language
- **Mission statement**: The long-term goal or north star
- **Key differentiators**: 3–5 bullets on what makes it different from alternatives

### 2. Tech Stack Summary
Broken into subsections by layer. Each entry includes:
- **Name + file/path** — where it lives
- **Complexity rating** — Low / Medium / High
- **One-sentence role** — what it does in this project
- **Notable behaviors** — anything non-obvious or project-specific

Common subsections:
- **Core Platform** — runtime, build tools, test framework
- **UI Stack** — framework, router, notifications, styling, component library, DnD
- **Key Components** — per-component entries for anything non-trivial
- **Stores / State** — global state management

### 3. File Structure
- Full annotated directory tree using code block
- Every non-trivial file has an inline `# comment` description
- Grouped to mirror the actual folder hierarchy exactly
- Omit generated/build output folders (dist, node_modules) unless relevant

### 4. Build & Tooling
- Packaging/CI tool and what it produces per platform
- Test runner setup notes (mocking strategy, coverage config)
- **Commands table**: every `npm run` / `make` / script with a plain-English description

### 5. Data & Storage
- **Storage format**: file naming convention, schema/frontmatter fields
- **Search/query engine**: library used, indexing strategy, scoring weights, key config values
- **Settings/config**: where stored, any sync or mirroring behavior

---

## Procedure

### Step 1 — Discover
Read (in parallel where possible):
- `package.json` — dependencies, scripts, name, version
- Root config files — `vite.config.*`, `tsconfig.json`, `tailwind.config.*`, etc.
- Entry points — `src/main.ts`, `electron/main.ts`, `index.html`
- Existing `docs/ARCHITECTURE.md` or `ARCHITECTURE.md` if present
- `README.md` for any stated mission/vision

### Step 2 — Explore Structure
Walk the directory tree (2–3 levels deep). Note:
- Where source code lives vs build output
- Manager / service / handler patterns
- Route files and component organization
- Store / state files

### Step 3 — Write Each Section
Follow the Output Structure above. Apply these rules:
- Lead each tech entry with: `**Name** (\`path\`) — Complexity`
- Use `---` dividers between major sections
- Use fenced code blocks for file trees and command tables
- Never pad with filler prose — every sentence must carry information

### Step 4 — Sync Check
If updating an existing ARCHITECTURE.md, diff against reality:
- New/removed/renamed files → update File Structure
- New/removed dependencies → update Tech Stack
- New/removed scripts → update Build & Tooling
- Schema changes → update Data & Storage
- Update the `Version` header if applicable

### Step 5 — Save
Write to `docs/ARCHITECTURE.md` (preferred) or `ARCHITECTURE.md` at root if no `docs/` folder exists.

---

## Quality Criteria
- [ ] All 5 sections present
- [ ] Every major file in the tree has an inline description
- [ ] Every `npm run` script is in the commands table
- [ ] Complexity ratings assigned to every tech entry
- [ ] No section describes something that no longer exists in the codebase
- [ ] The document can fully orient a new developer without any other reference
