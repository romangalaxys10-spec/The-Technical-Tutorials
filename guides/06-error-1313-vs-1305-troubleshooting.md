# 🔍 Diagnosing API Errors: Error 1313 (FUP Lock) vs Error 1305 (Capacity Surge)

> **Part of [The Technical Tutorials](https://github.com/romangalaxys10-spec/The-Technical-Tutorials)** collection by the Z.ai Ambassador Team.

---

## 📌 Technical Distinction

| Error Code | HTTP Status | Meaning | Action Required |
| :--- | :--- | :--- | :--- |
| **Error 1313** | `HTTP 429` | Account Fair Usage Policy (FUP) restriction triggered by automated retry loops or multi-agent concurrency. | Revoke API keys, stop automated retry loops, and wait for the 30-day rolling evaluation cooldown. |
| **Error 1305** | `HTTP 429` | Momentary GPU cluster capacity surge during peak traffic waves. **Account is NOT locked**. | Pause 30–60 seconds, trim workspace file context (128k–256k limit), and retry. |

---

## ⚡ How to Prevent API Throttling in Harness IDEs (OpenCode / ZCode)

1. **Disable Automated Retry Loops**: Set max retry count to 0 or 1 in client settings to prevent infinite loop flags.
2. **Trim Context Weight**: Attach only active files rather than full repository indexing.
3. **Avoid Parallel Agents**: Run single-session agent calls during 3x peak multiplier windows (14:00–18:00 UTC+8).
