# Contributing to Subnetting

Thanks for helping make subnetting easier to learn. Bug reports, ideas, docs fixes and code are
all welcome.

## Before you start

- Check the [open issues](../../issues) and the [roadmap](docs/ROADMAP.md) to avoid duplicate work.
- For anything bigger than a small fix, open an issue first so we can agree on the approach.
- Security problems go through [SECURITY.md](SECURITY.md), not public issues.

## Local setup

Requirements: Node.js 24 (see `.nvmrc`) and npm.

```bash
git clone https://github.com/syednoorulhassan001/Subnetting.git
cd Subnetting
npm ci
npm run dev
```

## Making a change

1. Fork the repository and create a branch from `main` (for example `fix/broadcast-for-31`).
2. Make your change in small, focused commits with clear messages.
3. Run `npm run check`. It runs lint, type-check, format check and tests, and CI runs the same.
4. Open a pull request and fill in the template.

## Ground rules

- **Subnet math lives in `src/lib/subnet`** and must stay free of React and browser APIs. Every
  change there needs unit tests, including edge cases such as `/0`, `/31` and `/32`.
- **Teach, don't just answer.** Features should show their working so learners understand why.
- **Accessibility matters.** Keep keyboard navigation working and respect
  `prefers-reduced-motion` for animations.
- **Keep dependencies lean.** Adding a package needs a good reason in the pull request.
- Format with Prettier (`npm run format`); don't hand-format.

## Reporting a wrong calculation

Open a bug report with the address and prefix you entered, what you expected, and what the app
showed. A reproducible example is the most useful thing you can send.
