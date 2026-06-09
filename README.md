<p align="center">
  <img src="./banner.jpg" alt="DOX" width="100%">
</p>

## How DOX works

DOX is a tiny CLAUDE.md framework that gives Claude Code precise project context.

Claude keeps a hierarchy of CLAUDE.md files as the project changes:

- root CLAUDE.md contains project-wide instructions and the top-level index
- child CLAUDE.md files contain local instructions for specific areas
- before any edit, Claude walks the docs tree from the root to the area it will touch
- the relevant docs give it exact local guidelines, so it does not edit blindly
- after meaningful changes, it updates the affected CLAUDE.md files

The result is simple: traverse the docs, understand the local rules, make precise edits, keep the docs current. Less guessing. Less drift. Less "why did it touch that file?"

## How to use

1. Copy the contents of [CLAUDE.md](./CLAUDE.md?plain=1) into your project's CLAUDE.md file.

<br>
That's it. No installation, no dependencies, no package, no runtime. DOX is just a Markdown instruction for Claude Code.

It works natively with Claude Code, which reads CLAUDE.md files for project memory and supports the nested hierarchy DOX relies on.

No CLAUDE.md yet? Copy the file into your project root. Claude will see these instructions and will start building the DOX tree.

For an existing project, you can tell Claude: `Initialize DOX tree for this project now.` It will create all the child CLAUDE.md files and indexes.

## Credits

<p align="center">
  Created by <strong><a href="https://www.agent-zero.ai/">Agent Zero</a></strong><br>
  Open-source agentic AI framework<br>
  <a href="https://www.agent-zero.ai/">Website</a> · <a href="https://github.com/agent0ai/agent-zero">GitHub repository</a><br>
  Claude Code adaptation of the original <a href="https://github.com/agent0ai/dox">DOX</a> framework
</p>
