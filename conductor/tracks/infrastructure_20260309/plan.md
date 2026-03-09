# Implementation Plan: Implement Core Infrastructure Scaffolding and Repository Pattern

## Phase 1: Engineering Infrastructure
- [ ] Task: [Scout] Existing `gemini-extension.json` and shell environment [Skills: Repo-Pattern-Enforcer] [MCP: Shell, Search]
    - [ ] Analyze the project structure to determine the best location for `src/`.
    - [ ] Check for existing linting or build tools in the environment.
- [ ] Task: Initialize Node/TS Scaffolding [Skills: Strict-Type-Auditor] [MCP: Shell, FileSystem]
    - [ ] Run `pnpm init`.
    - [ ] Install `typescript`, `vitest`, `eslint`, `prettier`, `dependency-cruiser`, `husky` as devDependencies.
    - [ ] Write `tsconfig.json` with `strict: true`, `noImplicitAny: true`, `strictNullChecks: true`, `noUnusedLocals: true`.
- [ ] Task: Configure Quality Gates [Skills: Strict-Type-Auditor] [MCP: FileSystem, Shell]
    - [ ] Set up `.eslintrc.json` with strict rules.
    - [ ] Configure `dependency-cruiser` to enforce architectural boundaries.
    - [ ] Initialize `husky` with a pre-commit hook for linting and testing.
- [ ] Task: Conductor - User Manual Verification 'Engineering Infrastructure' (Protocol in workflow.md)

## Phase 2: Repository Pattern Foundation
- [ ] Task: [Scout] Existing `FileSystem` usage in `conductor/` folder [Skills: Repo-Pattern-Enforcer] [MCP: Search, FileSystem]
    - [ ] Identify all points where the extension reads or writes to the `conductor/` directory.
- [ ] Task: Write Tests for FileSystemRepository [Skills: Repo-Pattern-Enforcer] [MCP: FileSystem]
    - [ ] Write failing unit tests for `readProductGuide()`, `writeProductGuide()`, and `exists(path)`.
    - [ ] Ensure tests use the "Anti-Mocking" philosophy (real temp directory).
- [ ] Task: Implement FileSystemRepository [Skills: Repo-Pattern-Enforcer] [MCP: FileSystem]
    - [ ] Implement the repository class to pass tests.
    - [ ] Verify 100% test coverage.
- [ ] Task: Conductor - User Manual Verification 'Repository Pattern Foundation' (Protocol in workflow.md)

## Phase 3: Final Scaffolding Verification
- [ ] Task: End-to-End Scaffolding Verification [Skills: Strict-Type-Auditor] [MCP: Shell]
    - [ ] Run `pnpm run check` (Lint + Type Check + Test) to ensure all gates are active.
    - [ ] Verify that `dependency-cruiser` correctly identifies the project structure.
- [ ] Task: Conductor - User Manual Verification 'Final Scaffolding Verification' (Protocol in workflow.md)
