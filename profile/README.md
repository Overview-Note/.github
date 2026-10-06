<div align="center">

<img src="https://raw.githubusercontent.com/Overview-Note/overview/main/web/public/icon.svg" width="72" alt="Overview" />

# Overview Note

**A self-hosted, folder-based Markdown knowledge base — files as the source of truth, AI-native, shipped as a single binary and a native desktop app.**

[📖 Documentation](https://overview-note.github.io/overview/) · [⬇️ Releases](https://github.com/Overview-Note/overview/releases) · [⭐ Source](https://github.com/Overview-Note/overview)

</div>

---

## What we build

**[Overview](https://github.com/Overview-Note/overview)** is what you get when you take the simplicity of [memos](https://github.com/usememos/memos), add the **hierarchy memos lacks**, and keep your content as **plain Markdown files you fully own**.

Every note is a Markdown file with YAML frontmatter on disk; the SQLite index is disposable and fully rebuildable, so Git, Obsidian or any editor can point at the same `data/` folder. Overview runs as **one Go binary with the frontend embedded** (or a single `docker run`) and as a **native desktop app** — no external services required.

> 自托管、以文件夹组织的 Markdown 知识库：**文件即真相**，AI 原生，单二进制 / 原生桌面应用。

## Feature highlights

| | |
|---|---|
| 📚 **Content** | Hierarchical folders · plain-Markdown source of truth · wiki-links & backlinks · per-note private/public |
| ✍️ **Editing** | Vue 3 + Tiptap editor · code highlighting · task lists · KaTeX math · Mermaid diagrams · images & attachments · slash commands · outline · focus mode |
| 🔎 **Search** | SQLite **FTS5** with a custom **CJK unigram + bigram** tokenizer (real substring matching) |
| 🤖 **AI-native** | OpenAI-compatible assistant (*organize* / *complete*) · **tool-calling agent** that performs in-app actions with human approval and an audit trail · **MCP server** (22 tools) |
| 🔐 **Access** | Multi-user auth (bcrypt, sessions, admin/member) · email invite / verification / password reset · optional self-registration · **REST API** (`/api/v1`, OpenAPI) · **WebDAV** · **PWA** with a responsive mobile layout |
| 🛠 **Operations** | Single binary · structured logging · version history & trash · live file-watcher reindex · portable vault archive · full CLI · **pluggable storage** (local or S3-compatible) |
| 🔄 **Sync** | Desktop ↔ server sync with **real-time SSE events**, incremental `/sync/changes`, three-way merge with conflict copies, and S3-backed assets |
| 🖥 **Desktop** | **Wails v3** shell (Windows · macOS · Linux) · system tray · `.md` file association · `overview://` deep links · onboarding wizard and a changeable vault · update notification |

## Get started

**Docker (server / self-host):**

```bash
docker run -d --name overview \
  -p 5230:5230 \
  -v "$PWD/data:/data" \
  ghcr.io/overview-note/overview:latest
```

Then open <http://localhost:5230>.

**Desktop app:** download the build for your platform from the [latest release](https://github.com/Overview-Note/overview/releases/latest) — Windows `.zip`, macOS `arm64`/`amd64`, Linux `amd64`.

**From source:** `go build ./cmd/overview` (the frontend is embedded). See the [documentation](https://overview-note.github.io/overview/).

## Tech stack

![Go](https://img.shields.io/badge/Go-1.26-00ADD8?logo=go&logoColor=white)
![Vue](https://img.shields.io/badge/Vue-3-42b883?logo=vuedotjs&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-FTS5-003B57?logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-multi--arch-2496ED?logo=docker&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)

## Links

- 📖 Documentation — <https://overview-note.github.io/overview/>
- ⬇️ Releases — <https://github.com/Overview-Note/overview/releases>
- 🐛 Issues — <https://github.com/Overview-Note/overview/issues>

<div align="center"><sub>MIT licensed · built with Go &amp; Vue</sub></div>
