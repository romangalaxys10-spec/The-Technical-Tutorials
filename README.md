# 🚀 The Technical Tutorials

Welcome to **The Technical Tutorials** repository—a curated collection of production-grade technical guides, AI agent workflow protocols, prompt engineering workarounds, and developer tools maintained by the **Z.ai Ambassador Team**.

---

## 📚 Technical Tutorials & Guides Index

| # | Guide Title | Topic / Scope | GFM Guide Link |
| :--- | :--- | :--- | :--- |
| **01** | **Mastering AI Agent Workflows: GitHub PAT Auto-Push Protocol** | Never lose code or chat history in ephemeral web containers (`chat.z.ai`, v0, Bolt.new, Lovable) or local IDEs. | [View Guide](./README.md) · [Web Article](https://claw.rommark.dev/blog/53-github-agent-workflow-tutorial.html) |
| **02** | **Universal Token Efficiency Protocol v3.3.0** | 8 behavioral pillars for `AGENTS.md` / `CLAUDE.md` that cut context consumption by 50–80% (280K &rarr; 35K tokens). | [View Guide](./guides/02-token-efficiency-protocol.md) |
| **03** | **Long-Horizon Agent Loop File Delivery & Tunnel Workaround** | Prompt workaround to generate public download URLs / tunnels for sandbox files. | [View Guide](./guides/03-long-horizon-file-tunnel-prompt.md) |
| **04** | **Marcos Hernanz Agentic Engineering Principles** | 8 core rules for building software cleanly with autonomous AI coding agents. | [View Guide](./guides/04-agentic-engineering-principles.md) |
| **05** | **Steve Jobs Product Design, Flow & Quality Standard** | 4 pillars for enforcing extreme simplicity, dark glassmorphism, and craftsman quality. | [View Guide](./guides/05-steve-jobs-design-quality-standard.md) |
| **06** | **Diagnosing API Errors: Error 1313 (FUP Lock) vs Error 1305 (Capacity Surge)** | Troubleshooting developer rate limits, 30-day rolling cooldowns, and OpenCode context tuning. | [View Guide](./guides/06-error-1313-vs-1305-troubleshooting.md) |
| **07** | **Ultra-Lightweight Local AWS Emulation with Floci Micro-VMs** | Test S3, DynamoDB, SQS, SNS, and Lambda locally (~13MB RAM, ~24ms boot) with zero AWS account required. | [View Guide](./guides/07-floci-local-aws-emulator.md) |

---

## ⚡ Featured Guide: GitHub PAT Auto-Push Protocol

### 🔑 Quickstart Step 1: Generate PAT
Create a classic GitHub Personal Access Token with **`repo`** scope.

### 🔗 Quickstart Step 2: Agent Backup Prompt
Send this directive to your web agent (`chat.z.ai`, v0, Bolt.new, Lovable) or local IDE:

```text
[SYSTEM DIRECTIVE: AUTOMATED WORKSPACE & CHAT HISTORY BACKUP PROTOCOL]
You are equipped with git access to my remote repository.

Mandatory Rules:
1. Whole Workspace Backup: Always maintain a complete backup of all project files, assets, scripts, data, and documentation.
2. Complete Chat History Backup: Save and update our full conversation history / session chat transcript as a file named `chat_history.md` (or `session_log.md`) in the project root after every turn.
3. Automated Git Sync: After modifying workspace files or writing response updates, immediately execute:
   git add .
   git commit -m "feat: update workspace files and append session chat history log"
   git push origin main
4. If a push fails due to remote divergence, run `git pull --rebase origin main` and re-push.
```

---

## 🤝 Contributing & Community

These tutorials are maintained by **[romangalaxys10-spec](https://github.com/romangalaxys10-spec)** and the Z.ai Ambassador team. Have a tutorial or prompt workaround to share? Open an Issue or Pull Request!

&copy; 2026 **Z.ai Ambassador Workspace** · Deployed at [claw.rommark.dev/blog](https://claw.rommark.dev/blog/)
