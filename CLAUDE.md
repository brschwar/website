# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Personal website for [brian.codes](https://brian.codes) — a single-page site used for job search. Primary users will be hiring professionals and people within my network to gain insight into my work history.

This project optimizes for:
- visual polish
- speed of iteration
- clean responsive code
- easy handoff to engineering

Avoid over-engineering. Prefer clarity over cleverness.

## Tech Stack

- React + TypeScript
- Nextjs with app router
- Tailwind CSS
- Shadcn/ui
- React hook form + Zod for forms
- Supabase for auth and data
- Vitest with React Testing Library (RTL) for unit testing
- Atomic Design methodology
- Playwright for visual testing

Do not introduce:
- Redux
- Styled components
- Material UI
Unless explicitly requested

## Architecture

- `app/` contains routes and server components
- `components/ui/` contains reusable deisng-system components
- `lib/` contains utilities, API helpers, and shared config
- `features/` contains feature-specific business logic
- `types/` contains shared TypeScript types

Rules:
- Move repeated UI into reusable components
- Keep side effects out of UI components when possible
- Prefer server-side data feteching unless client inteactivity is required
- Do not create a new abstraction for one-off usage
- Prefer editing existing components over creating near-duplicates
- Preserve backward compatibility for shared components unless directed
- Flag major architectural changes before implementing them

### File Placement Rules

- Add reusable primitives to `src/components/ui`
- All components live in `src/components/{atoms|molecules|organisms}/`
- Keep page-level composition in route files


### Running locally

Install: `pnpm install`
Dev: `pnpm dev`
Build: `pnpm build`
Lint: `pnpm lint`
Typecheck: `pnpm typecheck`
Test: `pnpm test`

### Code Conventions:

- **TypeScript / React:**
  - Prefer functional components
  - Prefer server components
  - Prefer named exports for shared modules
  - Use async/await instead of chained promises
  - Keep components focused and composable
  - Extract repeated logic into hooks or helpers
  - Prefer descriptive variable names over abbreviations
  - Add comments only when intent is non-obvious
  - Do not leave dead code or commented out blocks
  - Use Tailwind utilities instead of custom CSS
  - No semicolons (enforced by `prettier`)
- **EditorConfig** 
  - 2-space indentation, UTF-8, LF line endings, trailing whitespace trimmed

### Anti-Patterns to Avoid:

- Do not use `any` in TypeScript; define strict types
- Never write nested ternary operators; use `if/else` or early returns


## Frontend & UI Rules
Before writing, modifying, or creating any UI components, frontend layouts, or CSS styles, you MUST read the [DESIGN.md](DESIGN.md) file located in the project root. Strictly adhere to the design tokens, framework rules, and component structures defined there. Do not invent custom UI values or styling rules outside of those guidelines.

## Content Guidelines
- Use concise, confident language
- Avoid hype and empty marketing phrases
- Headlines should be clear before cleaver
- Body copy should focus on user outcomes
- Prefer short paragraphs and scannable structure
- Avoid jargon unless it is understood by the target audience