# DOX for Claude Code

This is an adaptation of the [DOX framework](https://github.com/agent0ai/dox) (originally built around `AGENTS.md`) reworked to run **natively inside Claude Code** using `CLAUDE.md` files.

Claude Code reads `CLAUDE.md` for project memory and supports a nested hierarchy of these files. This adaptation converts the entire DOX contract from `AGENTS.md` to `CLAUDE.md` so the framework works out of the box with Claude Code — no extra config, no plugins.

## How DOX works

DOX is a tiny `CLAUDE.md` framework that gives Claude Code precise project context.

Claude keeps a hierarchy of `CLAUDE.md` files as the project changes:

- root `CLAUDE.md` contains project-wide instructions and the top-level index
- child `CLAUDE.md` files contain local instructions for specific areas
- before any edit, Claude walks the docs tree from the root to the area it will touch
- the relevant docs give it exact local guidelines, so it does not edit blindly
- after meaningful changes, it updates the affected `CLAUDE.md` files

The result is simple: traverse the docs, understand the local rules, make precise edits, keep the docs current. Less guessing. Less drift. Less "why did it touch that file?"

## How to use

1. Copy the contents of [CLAUDE.md](./CLAUDE.md?plain=1) into your project's root `CLAUDE.md` file.

That's it. No installation, no dependencies, no package, no runtime. DOX is just a Markdown instruction Claude Code reads automatically.

No `CLAUDE.md` yet? Copy the file into your project root. Claude will see these instructions and start building the DOX tree.

For an existing project, tell Claude: `Initialize DOX tree for this project now.` It will create all the child `CLAUDE.md` files and indexes.

## Credits

Original DOX framework created by **[Agent Zero](https://www.agent-zero.ai/)** — open-source agentic AI framework ([Website](https://www.agent-zero.ai/) · [GitHub](https://github.com/agent0ai/agent-zero)).

This repository is a Claude Code adaptation of the original [DOX](https://github.com/agent0ai/dox).
