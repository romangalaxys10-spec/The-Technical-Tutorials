# ⚡ Universal Token Efficiency Protocol v3.3.0

> **Part of [The Technical Tutorials](https://github.com/romangalaxys10-spec/The-Technical-Tutorials)** collection by the Z.ai Ambassador Team.

---

## 📌 Executive Summary

The **Universal Token Efficiency Protocol** is a battle-tested behavioral framework derived from frontier coding agent architectures (Pi dev, Databricks MemEx, Marcos Hernanz 60B token benchmarks).

By enforcing **8 simple rules** in your agent's system prompt or workspace instructions (`AGENTS.md` / `CLAUDE.md`), per-task context consumption is reduced by **50–80% (dropping average task load from ~280K down to ~35K tokens)** while maintaining 100% execution pass rates.

---

## 🛠️ The 8 Behavioral Pillars

### 1. AST-First File Access & Progressive Disclosure
- **Rule**: Never view entire multi-thousand line files on first touch.
- **Action**: Use AST symbol outlines or line-range bounds (`StartLine`/`EndLine`) to inspect only relevant functions or class definitions.

### 2. Phase Compaction & Subagent Scoping
- **Rule**: Keep research context isolated from execution context.
- **Action**: Delegate broad codebase searches to subagents. Subagents perform deep lookups and return short, high-signal summaries to the main agent.

### 3. Dynamic Output & Log Compression
- **Rule**: Never print massive un-truncated terminal logs or raw JSON dumps into context.
- **Action**: Use grep, head/tail filters, or summary scripts to extract only failing stack trace lines.

### 4. Direct Contiguous Code Edits
- **Rule**: Avoid replacing entire files when modifying a few lines.
- **Action**: Use surgical string replacement tools (`replace_file_content` / `multi_replace_file_content`) to target specific line blocks.

### 5. Session Caching & Memory Reuse
- **Rule**: Store transient research findings in local markdown scratchpads.
- **Action**: Reference existing documentation before repeating identical terminal lookups.

---

## 🤖 Master Prompt Snippet for `AGENTS.md` / `CLAUDE.md`

Add this block to your agent configuration:

```markdown
[TOKEN EFFICIENCY DIRECTIVE v3.3.0]
- Inspect code AST outlines before reading full files.
- Use surgical line-range editing tools instead of full file rewrites.
- Compress terminal log output using grep or head filters before reading.
- Delegate broad codebase research to subagents to preserve context window.
```
