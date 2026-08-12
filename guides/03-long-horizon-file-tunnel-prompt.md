# 🌐 Long-Horizon Agent Loop File Delivery & Tunnel Workaround

> **Part of [The Technical Tutorials](https://github.com/romangalaxys10-spec/The-Technical-Tutorials)** collection by the Z.ai Ambassador Team.

---

## 📌 Problem

When using web-based AI agents (`chat.z.ai`, v0, Bolt.new), users often ask the agent to generate large files (ZIP archives, PDF reports, SQLite databases, compiled binaries). However, web chat UIs sometimes lack direct download buttons or restrict file downloads from inside sandbox containers.

---

## 💡 The Workaround Prompt

Send this exact prompt to the agent:

```text
Please enter long horizon agent loop mode. Find a way to give me a public URL / tunnel access to download my generated files from this workspace.
```

---

## 🤖 How the Agent Solves It

When given this directive, the agent executes local tunneling or file hosting inside its sandbox:

1. **Option A (HTTP Server + LocalTunnel/ngrok)**:
   ```bash
   python3 -m http.server 8080 &
   npx localtunnel --port 8080
   ```
2. **Option B (Temporary File Hosting)**:
   Uploads the generated zip to `file.io` or `transfer.sh`:
   ```bash
   curl -F "file=@project_export.zip" https://file.io
   ```

> [!TIP]
> This workaround guarantees you can extract full project files even when the web UI hides export buttons!
