# 🦞 The Survival Guide (Lobster Edition)

> **Warning**: Not official docs. These are "wild" hacks for survival.
> *如果你想马上跑通，看这个。*

---

## ⚡️ 30s Speed Run (极速启动)

Don't read manuals. Just run this:

### 1. The One-Liner (Linux/Mac)
```bash
curl -sL https://openclaw.ai/install | bash -s -- --wizard
```
*   **Feature**: Auto-detects environment, pulls default skills.
*   **Stuck on Port 22?**: It auto-switches to Rootless mode. Safe & fast.

### 2. Windows Users (WSL2 Only)
Do not use PowerShell directly.
1.  Install **WSL 2** (Ubuntu 22.04).
2.  Run the command above inside WSL.
3.  Trust me, this saves you 3 days of pain.

---

## 🚑 The Clinic (急救室)

### Symptom: `WebSocket 1006` (Crash on Start)
*   **Diagnosis**: Broken plugin config (usually Discord).
*   **Fix**:
    ```bash
    openclaw doctor --fix
    ```
    *This command scans your config and comments out broken parts.*

### Symptom: Discord "Not Available"
*   **Diagnosis**: Missing permissions.
*   **Fix**: Go to Discord Dev Portal -> Bot -> Enable **Message Content Intent**.

### Symptom: AI is Dumb / Hallucinating
*   **Diagnosis**: Context Poisoning.
*   **Fix**: `/reset` (Ralph Wiggum Mode - Force context clear).

---

## 🇨🇳 China Special (国内特供)

### Docker Mirror (镜像加速)
Add to `/etc/docker/daemon.json`:
```json
{
  "registry-mirrors": [
    "https://docker.m.daocloud.io",
    "https://huecker.io",
    "https://dockerhub.timeweb.cloud"
  ]
}
```
*Restart Docker: `sudo systemctl restart docker`*

### Model Source (模型源)
*   Use **Ollama** locally.
*   Use **DeepSeek API** (fast & cheap).
