<div align="center">

<img src="https://gitrama.ai/assets/logo.svg" alt="Gitrama" width="80" />

# Gitrama

**AI-powered Git intelligence from your terminal.**

Smart commits · Branch naming · PR descriptions · Changelogs · Codebase chat · Stream workflows

[Website](https://gitrama.ai) · [Documentation](https://gitrama.ai/docs) · [PyPI](https://pypi.org/project/gitrama/) · [Changelog](https://gitrama.ai/releases)

---

</div>

## What is Gitrama?

Gitrama is a CLI tool that brings AI directly into your Git workflow. It analyzes your code changes, understands your repository's history, and generates commit messages, branch names, PR descriptions, and changelogs — all from the terminal.

No browser tabs. No context switching. No copy-pasting diffs into ChatGPT.

```
$ gtr commit
┌─ Analyzing staged changes...
│  src/auth.py  (+42 -18)  ─  OAuth2 PKCE flow implementation
│  tests/test_auth.py  (+67 -0)  ─  New test coverage
│
└─ feat(auth): implement OAuth2 PKCE flow with token refresh
   
   - Add PKCE challenge/verifier generation for secure authorization
   - Implement token refresh logic with exponential backoff
   - Add comprehensive test coverage for auth flow edge cases
   
   Refs: #142

✅ Committed to feat/user-auth (a3f8c2d)
```

## Products

| Product | Description | Install |
|---------|-------------|---------|
| **[Gitrama CLI](https://github.com/onegreatdev/gitrama)** | The core tool. AI commits, branches, PRs, changelogs, and codebase chat. | `pip install gitrama` |
| **[Gitrama MCP Server](https://github.com/onegreatdev/gitrama-mcp)** | MCP integration for Cursor, Claude Desktop, VS Code, and other AI IDEs. | `pip install gitrama-mcp` |

## Core Commands

| Command | What it does |
|---------|-------------|
| `gtr commit` | Generate an AI commit message from your staged diff |
| `gtr chat` | Talk to your repository — ask questions about code, history, ownership |
| `gtr branch --suggest` | Get AI-suggested branch names from a task description |
| `gtr pr` | Generate a full PR description from your branch diff |
| `gtr changelog` | Generate a grouped changelog between any two refs |
| `gtr stream` | Manage workflow context — switch focus, carry context across commands |
| `gtr autopilot` | Watch for changes and auto-commit with AI messages |
| `gtr config` | Configure providers, models, and preferences |

## How It Works

Gitrama wraps your existing Git workflow. It reads your diffs, staged changes, branch history, and commit log — then uses AI to generate contextual, high-quality output. Nothing is sent to the cloud unless you choose a cloud provider. Local models (Ollama) are fully supported.

```
Your code changes
       ↓
   Git diff analysis
       ↓
   AI context assembly (diff + history + branch + config)
       ↓
   Model inference (OpenAI / Anthropic / Ollama / custom)
       ↓
   Structured output (commit msg / PR / changelog / chat response)
```

## IDE Integration (MCP)

Gitrama works inside your AI-powered editor through the [Model Context Protocol](https://modelcontextprotocol.io):

**Cursor** · **Claude Desktop** · **Claude Code** · **Windsurf** · **VS Code** · **Zed**

```json
{
  "mcpServers": {
    "gitrama": {
      "command": "gitrama-mcp"
    }
  }
}
```

10 tools available: `gitrama_commit` · `gitrama_stage_and_commit` · `gitrama_commit_quality` · `gitrama_branch` · `gitrama_branch_suggest` · `gitrama_pr` · `gitrama_changelog` · `gitrama_stream_status` · `gitrama_stream_switch` · `gitrama_stream_list`

## Supported AI Providers

| Provider | Models | Setup |
|----------|--------|-------|
| **OpenAI** | GPT-4o, GPT-4o-mini, o1, o3 | `gtr config --provider openai --key sk-...` |
| **Anthropic** | Claude Sonnet, Claude Haiku | `gtr config --provider anthropic --key sk-ant-...` |
| **Ollama** | Llama 3, Mistral, CodeLlama, Qwen | `gtr config --provider ollama --model llama3` |
| **Custom** | Any OpenAI-compatible endpoint | `gtr config --provider custom --base-url http://...` |

## Install

```bash
# Python (all platforms)
pip install gitrama

# macOS / Linux (coming soon)
brew install gitrama

# Universal (coming soon)
curl -fsSL https://gitrama.ai/install.sh | sh
```

## Pricing

| Tier | Price | What you get |
|------|-------|-------------|
| **Free** | $0 | Core commands, 90-day search, community support |
| **Pro** | $9/mo | Full history, deep analysis, session sharing, priority support |
| **Enterprise** | Contact us | Team dashboards, SSO, on-premise, custom models |

## Built By

Gitrama is built by [Alfonso Harding](https://linkedin.com/in/alfonsoharding) — 20 years in software engineering, from startups to Fortune 500. Gitrama is his first solo product, built to solve the problems he saw every day across decades of shipping code.

## Links

- 🌐 [gitrama.ai](https://gitrama.ai)
- 📦 [PyPI — gitrama](https://pypi.org/project/gitrama/)
- 📦 [PyPI — gitrama-mcp](https://pypi.org/project/gitrama-mcp/)
- 📖 [Documentation](https://gitrama.ai/docs_v4)
- 📝 [Release Notes](https://gitrama.ai/releases)
- 💼 [LinkedIn](https://www.linkedin.com/in/alfonso-h-47396b5/)

---

<div align="center">

🌿

*The companies that passed on the developer who built this will pay as customers.*

</div>
