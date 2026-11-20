# Roadmap

The project is built in small daily steps. Every day ends with a push to `main` (through a pull
request once branch protection is on) so the history stays easy to review.

## Day 0: Repository and foundation

- [ ] Scaffold Vite + React + TypeScript, add Vitest and Prettier
- [ ] README, LICENSE, CONTRIBUTING, CODE_OF_CONDUCT, SECURITY
- [ ] Issue and PR templates, CODEOWNERS
- [ ] CI (lint, type-check, format, test, build), Dependabot, dependency review
- [ ] GitHub security settings (private reporting, code scanning, secret scanning, branch rules)

## Day 1: Subnet math core

Pure TypeScript in `src/lib/subnet`, no UI.

- [ ] Parse and format IPv4 addresses, convert prefix and mask both ways
- [ ] Network, broadcast, first and last usable host, host count, wildcard mask
- [ ] Edge cases: /0, /31 (RFC 3021), /32, invalid input
- [ ] Thorough unit tests; remove the Day 0 smoke test

## Day 2: App shell and first deploy

- [ ] React Router with `HashRouter`, layout, navigation, empty pages
- [ ] Design tokens, light and dark theme, responsive base
- [ ] GitHub Pages deploy workflow, so the live site exists from the start

## Day 3: Calculator, first version

- [ ] Address and prefix input with validation
- [ ] Results: network, broadcast, host range, hosts, masks
- [ ] Copy buttons, shareable URL

## Day 4: Calculator shows its work

- [ ] Binary view of address and mask, the AND step highlighted
- [ ] Block-size ("magic number") explanation
- [ ] Plain-language explanation under each result

## Day 5: Quiz engine

- [ ] Seeded random generator, pure and tested
- [ ] Question types: host count, network address, broadcast address, same subnet or not
- [ ] Each question carries its worked solution

## Day 6: Quiz page

- [ ] Question in the center, answer hidden until the learner tries
- [ ] Reveal with steps, "Next question" button
- [ ] Difficulty levels, streak stored in the browser

## Day 7: Odometer engine

- [ ] Keyframe generator: slow start, first carry, double carry, jump to the end
- [ ] One-line caption for every stage
- [ ] Unit tests for the keyframe sequences (/8, /16, /24)

## Day 8: Odometer page

- [ ] Four octets with slide animation, binary bits underneath
- [ ] Network bits locked, host bits rolling
- [ ] Play, pause, step, speed, reduced-motion support

## Day 9: Odometer interaction

- [ ] Prefix slider that locks and unlocks bits
- [ ] Predict mode ("what comes next?")
- [ ] Link from the calculator and the quiz via the URL

## Day 10: About page

- [ ] IPv4 history: classful addressing, CIDR, address exhaustion
- [ ] Binary primer and a powers-of-two reference

## Day 11: Polish

- [ ] Accessibility pass (keyboard, screen reader, contrast)
- [ ] Mobile layouts, performance, page titles and social preview

## Day 12: Release

- [ ] Subnet-jump mode for non-octet prefixes such as /26
- [ ] Screenshots in the README, `v0.1.0` tag, release notes
- [ ] Label "good first issue" tasks for new contributors