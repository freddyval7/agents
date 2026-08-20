# OPENCODE AGENTS BY FTDEV7

Custom global agents for [opencode](https://opencode.ai).

## Available agents

| Agent   | Description |
|---------|-------------|
| `mentor` | Socratic senior mentor for junior developers. Socratic method, "why-first" explanations, mini-quizzes, guided code review, and automatic technology detection. Model: `opencode-go/qwen3.7-plus`. |

## Installation

Agents are placed in opencode's global agents directory:

- **Windows**: `%USERPROFILE%\.config\opencode\agents\`
- **macOS / Linux**: `~/.config/opencode/agents/`

### Option 1: Clone directly as the agents directory

```bash
# Windows (PowerShell)
git clone https://github.com/YOUR_USERNAME/opencode-agents.git "$env:USERPROFILE\.config\opencode\agents"

# macOS / Linux
git clone https://github.com/YOUR_USERNAME/opencode-agents.git ~/.config/opencode/agents
```

### Option 2: Clone elsewhere and create a symlink

```bash
# macOS / Linux
git clone https://github.com/YOUR_USERNAME/opencode-agents.git ~/opencode-agents
ln -s ~/opencode-agents ~/.config/opencode/agents
```

### Option 3: Manual copy

Download the `.md` file(s) and place them directly in `~/.config/opencode/agents/`.

## Update

```bash
cd ~/.config/opencode/agents
git pull
```

## Usage

After installing and restarting opencode:

- **As a primary agent**: switch to the `mentor` agent from the opencode interface.
- **As a subagent**: invoke `mentor` from any other agent via the Task tool.

## Adding a new agent

1. Create a `name.md` file at the root of this repository.
2. Add the frontmatter with `name`, `model`, `mode`, `description`, and `permission`.
3. Write the prompt in the file body.
4. Add a row to the agents table in this README.
5. Commit and push.
