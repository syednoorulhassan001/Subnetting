# Subnetting

Learn IPv4 subnetting step by step: a calculator that shows its work, a practice quiz, and an
odometer-style visualizer that makes octet rollover finally click.

[![CI](https://github.com/syednoorulhassan001/Subnetting/actions/workflows/ci.yml/badge.svg)](https://github.com/syednoorulhassan001/Subnetting/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

> **Status:** early development. The project is being built in small daily steps; see the
> [roadmap](docs/ROADMAP.md). Nothing is usable yet.

## Why this exists

Subnetting is easy to get lost in. Most tools hand you the answer without showing the math behind
it. This project started with a CCNA student who kept losing the thread, and it aims to teach the
reasoning, not just the result. It is free, open source, and runs entirely in your browser.

## Planned features

- **About**: a short history of IPv4 addressing and the theory you need (binary, masks, CIDR).
- **Calculator**: enter an address and prefix, see the network, broadcast, host range and the
  working behind each value.
- **Quiz**: endless practice questions (hosts per subnet, network address, and more). Try first,
  then reveal the answer with the steps.
- **Visual**: an odometer that shows how octets fill and roll over, for example why the last
  usable host in `1.0.0.0/8` is `1.255.255.254`.

## Tech stack

React, TypeScript, Vite, Vitest. There is no backend: everything runs client side.

## Getting started

Requirements: Node.js 24 (see `.nvmrc`; with [nvm](https://github.com/nvm-sh/nvm) run `nvm use`)
and npm.

```bash
git clone https://github.com/syednoorulhassan001/Subnetting.git
cd Subnetting
npm ci
npm run dev
```

### Scripts

| Command              | What it does                                               |
| -------------------- | ---------------------------------------------------------- |
| `npm run dev`        | Start the dev server                                       |
| `npm run build`      | Type-check and build for production                        |
| `npm run preview`    | Preview the production build locally                       |
| `npm test`           | Run the unit tests once                                    |
| `npm run test:watch` | Run the tests in watch mode                                |
| `npm run lint`       | Lint with ESLint                                           |
| `npm run typecheck`  | Type-check with TypeScript                                 |
| `npm run format`     | Format all files with Prettier                             |
| `npm run check`      | Lint, type-check, format check and tests (run before a PR) |

## Project structure

This is the planned layout and will fill in as the days go by.

```text
src/
  lib/subnet/   pure TypeScript subnet math (no React), fully unit tested
  pages/        About, Calculator, Quiz, Visual
  components/   shared UI pieces
docs/           roadmap and project notes
```

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) first, and follow the
[Code of Conduct](CODE_OF_CONDUCT.md).

## Security

Found a vulnerability? Please do not open a public issue. See [SECURITY.md](SECURITY.md).

## License

[MIT](LICENSE)
