# g1t Development Guidelines

> A minimal CLI for recording your commits.

## Project Overview

g1t is a single-file Node.js CLI with no dependencies. The whole program is `index.js`,
exposed as the `g1t` bin in package.json. There is no build step and no test suite: to
verify a change, run `node index.js` and check the output.

The current release is a stub that prints a banner and reserves the command name.

### Terminal Management

- **Always use background terminals** (`isBackground: true`) for every command so a terminal ID is returned
- **Always kill the terminal** after the command completes, whether it succeeds or fails — never leave terminals open
- Do not reuse foreground shell sessions — stale sessions block future terminal operations in Codespaces
- In GitHub Codespaces, agent-spawned terminals may be hidden — they still work. Do not assume a terminal is broken if you cannot see it
- If a terminal appears unresponsive, kill it and create a new one rather than retrying in the same terminal

## Contributing

- Follow the existing code style
- Test changes before submitting PRs
- Update documentation when adding features
- See [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines
