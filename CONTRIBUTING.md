# Contributing

Thank you for your interest in this project. This guide describes how to
report issues, propose changes, and open pull requests in a way that keeps
reviews efficient and the codebase healthy.

## Before you start

- Read the **[LICENSE](LICENSE)**. The software is offered under a **preview /
  evaluation** license; ensure your intended use aligns with it.
- Follow the **[Code of Conduct](CODE_OF_CONDUCT.md)** in all interactions.
- **Security-sensitive findings** must not be filed as public issues. Use the
  process in **[SECURITY.md](SECURITY.md)** instead.

## Reporting bugs

Use **Bug report** in the issue chooser (see
[`.github/ISSUE_TEMPLATE`](.github/ISSUE_TEMPLATE)). Include:

- What you expected vs. what happened
- Steps to reproduce, environment (OS, Node version), and relevant logs or
  screenshots
- Whether the issue is in `frontend/`, `studio/`, or both

## Suggesting features

Use **Feature request** in the issue chooser. Describe the problem you are
solving, proposed behavior, and any alternatives you considered. For larger
changes, opening an issue **before** writing code helps avoid rework.

## Pull requests

1. **Branch from the default branch** using a clear name (e.g.
   `fix/login-redirect`, `docs/api-examples`).
2. **Keep changes focused**—one logical concern per PR when practical.
3. **Match existing style**: formatting, naming, and patterns used nearby.
4. **Update docs** when behavior, env vars, or APIs change (see `docs/` and
   relevant READMEs).
5. **Do not commit secrets**: no real API keys, tokens, or production `.env`
   files (use `.env.example` patterns only).

PRs use the [pull request template](.github/pull_request_template.md). Fill it
out so reviewers can understand scope and risk quickly.

### Development setup

From the repository root:

```bash
npm install
npm run dev
```

Further prerequisites and workspace layout are in the root **[README.md](README.md)**
and **[docs/](docs/)**.

### Checks

Run project-local checks before requesting review when applicable (for example,
`npm run lint --workspace=frontend` and type generation/build steps described in
workspace READMEs).

## Review process

Maintainers may request changes or clarification. Keeping discussions respectful
and constructive aligns with the Code of Conduct.

## Questions

If something is unclear in this document or in the templates, open a **blank**
issue (with a `question` label if available) or use repository discussions when
enabled. Use **[SECURITY.md](SECURITY.md)** only for vulnerability reports.
