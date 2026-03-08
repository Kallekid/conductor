# Contributing to Conductor SDLC

Thank you for your interest in contributing to **Conductor SDLC**! As a fork focused on professional SDLC orchestration, we maintain high standards for code quality and architectural integrity.

## Our Philosophy

1. **Repository Pattern**: All data access must be abstracted.
2. **Anti-Mocking**: Tests should use real data/environments whenever possible.
3. **Strictness**: No implicit `any`, strict null checks, and comprehensive linting are mandatory.
4. **Scouting**: Always check for existing infrastructure before adding new logic.

## How to Contribute

1. **Fork the Repository**: Create your own fork of `conductor-sdlc`.
2. **Create a Track**: Use `/conductor:newTrack` to define your feature or fix.
3. **Follow the Workflow**: Adhere to the TDD and PR process defined in `conductor/workflow.md`.
4. **Submit a PR**: Ensure all quality gates (tests, linting, `pnpm audit`) pass before submitting.

## Code of Conduct

Please be respectful and professional in all interactions.

## Credits

This project is built upon the foundation of the original [Conductor](https://github.com/gemini-cli-extensions/conductor) project. We thank the original authors for their work.
