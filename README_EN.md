<div align="center">

<img src="docs/images/logo.png" width="128" height="128" alt="WujiTerm Logo" />

# WujiTerm

**Next-Generation High-Performance Smart Terminal & All-in-One Engineering Workbench for Developers, DevOps & SREs**

*Unifying SSH Terminal, Multi-Hop Bastion Automation, Live Kubernetes Log Diagnostics, Command Blocks, AI Ops Copilot, SQL & Redis Data Studio, SFTP/Pod File Transfer, and End-to-End Encrypted Cloud Sync in one fast native desktop app*

[![Platform](https://img.shields.io/badge/Platform-macOS%20Universal%20%7C%20Windows%20x86__64-0EA5E9?style=flat-square)](https://github.com/CoolwjSoft/wuji-term/releases)
[![Experience](https://img.shields.io/badge/Experience-Native%20Speed%20%7C%20Fluid%20Rendering-10B981?style=flat-square)](#why-wujiterm)
[![Security](https://img.shields.io/badge/Security-OS%20Keychain%20%7C%20Local%20Encrypted%20Vault-6366F1?style=flat-square)](#7-enterprise-security-audit--encrypted-sync)
[![License](https://img.shields.io/badge/License-MIT-64748B?style=flat-square)](#license)

**[简体中文](README.md)** | **English**

[Why WujiTerm](#why-wujiterm) · [Visual Tour](#visual-tour) · [Full Feature Breakdown](#full-feature-breakdown) · [Shortcuts](#keyboard-shortcuts) · [CLI & Private Sync](#8-wuji-cli--self-hosted-sync-server) · [Installation](#download--installation)

</div>

---

## Why WujiTerm?

During real-world development and production troubleshooting, engineers constantly switch between **SSH terminals, jump-host login scripts, log viewers, online JSON/SQL formatters, diff tools, database clients, Redis browsers, SFTP tools, file-transfer utilities, and AI chat tabs**. Fragmented tools break focus, while bloated terminal apps often lag and consume heavy memory under high-throughput log streams.

**WujiTerm** is a fast, lightweight native desktop terminal and all-in-one engineering workbench designed for developers, DevOps, and SREs — launching instantaneously, staying butter-smooth under massive log output, and unifying daily terminal sessions, log diagnostics, database queries, file transfers, and AI assistance inside one clean workspace:

| Scenario | Traditional Fragmented Tools | WujiTerm |
| :--- | :--- | :--- |
| **Heavy Log Throughput** | Stutters, drops frames, high memory & battery drain | **Hardware-accelerated native rendering**, ultra-smooth on massive logs, minimal idle footprint |
| **Multi-Hop Bastion & K8S** | Manual node selection, repeated passwords, shifting Pod IDs | **Reusable Jump Host inheritance + Visual Auto-Login + Smart Running Pod selector** |
| **Live Log Troubleshooting** | Manual scrolling, stream-breaking `grep`, risky online formatters | **Log syntax highlight + non-blocking `TraceId` Live Filter + 8 built-in formatters + Diff + Sanitized Copy** |
| **Modern Terminal Ergonomics** | Hard to edit long commands or isolate command outputs | **Command Blocks + Multi-line Smart Composer + Autocomplete + Cross-Session Visual History** |
| **Database & File Ops** | Separate SQL / Redis / SFTP / `rz/sz` apps | **Built-in MySQL / PG / ClickHouse / Redis Studio + SFTP & Bastion-penetrating Pod Transfer** |
| **AI Ops Assistance** | Copy-pasting stack traces to web chats, risking token leaks | **Built-in Multi-LLM AI Copilot** with auto error detection, pre-send sanitization & NL-to-Shell |
| **Security & Multi-Device Sync** | Plaintext configs or locked-in proprietary cloud accounts | **OS Keychain / Local Encrypted Vault + Prod Command Guardrail + Multi-Backend E2EE Sync** |

---

## Visual Tour

### 1. Unified Hosts Vault & Bastion Hub
> Single-row immersive titlebar merging native window controls with open tabs, manually reorderable sidebar Assets & Host Groups, Grid/List views, reusable jump-host inheritance, and multi-step automation pipelines.

<p align="center">
  <img src="docs/images/showcase-vault.jpg" alt="WujiTerm Hosts Vault & Bastion Hub" width="96%" />
</p>

### 2. Smart Terminal, Live Log Filter & AI Ops Copilot
> Arbitrary split panes with multi-pane broadcast input, real-time log syntax highlighting, bottom `TraceId` Live Log Filter drawer, and right-side AI root-cause diagnosis & fix panel.

<p align="center">
  <img src="docs/images/showcase-terminal.jpg" alt="WujiTerm Smart Terminal, Live Log Filter & AI Ops Copilot" width="96%" />
</p>

### 3. Integrated SQL / Redis Data Studio & SFTP / Pod File Transfer
> Connect directly to MySQL, PostgreSQL, ClickHouse, and Redis inside the same tab strip (with Read-Only Guardrails & Redis namespace tree), paired with the SFTP & bastion-penetrating Pod file transfer slide-over drawer.

<p align="center">
  <img src="docs/images/showcase-data-studio.jpg" alt="WujiTerm SQL & Redis Data Studio and SFTP File Explorer" width="96%" />
</p>

---

## Full Feature Breakdown

### 1. Fluid Terminal Experience & Modern Immersive Desktop UX

- **Fast, Fluid & Power-Efficient**
  - Hardware-accelerated rendering with full 24-bit TrueColor and crisp centered CJK typography — keeping massive log output smooth and responsive while consuming virtually zero resources when idle.
- **Unified Single-Row Immersive Titlebar (macOS & Windows)**
  - **macOS**: Native red/yellow/green window controls sit directly inside the single-row tab bar with clean vertical alignment, automatically collapsing left spacing in native Full Screen mode.
  - **Windows**: Eliminates redundant titlebars and extra menu rows into one sleek header — compact `☰` cascading menu button on the left and authentic `─ / □ / ✕` caption controls on the right, preserving native rounded corners, drop shadows, 8-edge border resizing, and window snapping.
  - Drag any empty header space to move the window; double-click to maximize or restore.
- **Flexible Tab Management, Pinning & Configurable `+` Button**
  - **3 Tab Bar Layout Modes**: (1) Single-row horizontal scroll; (2) Trailing `▾ More (N)` overflow dropdown (automatically keeps the active session visible); (3) Automatic multi-row wrap so all open tabs stay visible at once.
  - **Tab Pinning & Drag-to-Reorder**: Pin critical production sessions to prevent accidental closure, drag tabs to reorder, and right-click to close other or right-side unpinned tabs.
  - **Dual-Action `+` Button**: Left-click defaults to opening a Local Terminal and can be configured (in Interface Settings or right from the popover) to launch any specific host from your Vault; **right-click `+` anytime to open a searchable Host List** for 1-click connection or setting a new left-click default.
  - **Customizable Right Toolbar**: Independently toggle visibility of Command Palette, Split Right/Down, Command Blocks, Live Filter, AI Copilot, Line Wrap, Log Highlight, Snippets, Search, Files (SFTP + Pod Transfer), and standalone `rz/sz` buttons.
- **Long-Line Log Modes & Precision Mouse Ergonomics**
  - **Line Wrap / Single-Line Horizontal Scroll (`⌥Z` / `Alt+Z`)**: Single-line mode provides a smooth bottom scrollbar, trackpad horizontal swipe, and `Shift + Wheel` scrolling to read long JSON payloads and stack traces without line breaks.
  - **IDE-Grade Mouse Controls**: Click anywhere on the command line to position the shell cursor accurately (supporting mixed CJK and wrapped lines); double-click to select words, triple-click to select lines, optional copy-on-select, and `⌘/Ctrl + Click` to open URLs directly in your browser.
- **Arbitrary Split Panes, Pane Zoom & Broadcast Input**
  - Nested horizontal/vertical splits, temporary single-pane Zoom (`⇧⌘↵` / `Ctrl+Shift+↵`), and multi-pane **Broadcast Input (`⇧⌘I` / `Ctrl+Shift+I`)** to type once and execute across multiple cluster nodes simultaneously.
- **Global Command Palette (`⇧⌘P` / `Ctrl+Shift+P`) & Custom Right-Click Menu**
  - Keyboard-first fuzzy search across all hosts, databases, Redis caches, snippets, diagnostic playbooks, color schemes, and actions.
  - Fully editable terminal right-click menu (add/remove items, reorder, insert separators, bind custom command shortcuts).

---

### 2. Hosts Vault & Multi-Hop Bastion / Kubernetes Automation

- **All Connection Assets in One Place**
  - Manage **SSH remote hosts, Bastion/Jump hosts, automated login pipelines, Local Shells (auto-discovered OS shells), MySQL / PostgreSQL / ClickHouse databases, and Redis caches**, plus automatic local SSH config discovery.
- **Reusable Jump Host Inheritance**
  - Mark any Bastion or Jump Host as **"Reusable as Jump Host"** so downstream servers and Kubernetes pods inherit its credentials, encrypted password, and pre-login steps with one click.
  - Supports both **in-session Relay jump** and **SSH `-J` tunnel jump** modes.
- **Visual Auto-Login Pipelines & Smart Running Pod Selection**
  - Visually configure post-login jumps, menu selections, and startup commands (such as entering a target pod and tailing logs) without writing fragile shell scripts.
  - **Dynamic `auto:service|fallback` Pod Matcher**: Automatically parses interactive bastion/K8S menus and prefers healthy `Running` pods by service name — unaffected when pod indices shift after deployments.
  - **Universal Prompt Detection & Snippet Integration**: Simply type `shell` to match macOS, Linux, and Windows shell prompts automatically, or `now` for immediate dispatch; pick commands straight from your Snippets library.
- **Flexible Views, Nested Groups & Full Manual Reordering**
  - Switch between **Grid Cards** and **Compact List** views with 5 sort modes (Custom order with `↑/↓`, Name A→Z / Z→A, Address, Protocol).
  - Organize hosts with nested folder groups (e.g. `Prod/OrderService`) and rename groups inline.
  - **Manual Reordering for Sidebar Assets & Host Groups**: Reorder both "Connection Assets" and "Host Groups" by **press-and-hold dragging**, toggling **`⇅ Sort` inline `↑/↓` buttons**, or using **right-click menus** (Move Up/Down/Top/Bottom); group order syncs across the entire Hosts Vault.
- **Production Safety & Reliability**
  - Host-level **`PROD` warning badges**, **Auto-Reconnect** with countdown & cancel, **Anti-Idle Heartbeat** to prevent bastion disconnects, and configurable **Launch Behavior** (Hosts Vault / Local Terminal / Specific Host).

---

### 3. Developer & SRE Diagnostics Workbench

- **Smart Terminal: Command Blocks & Multi-Line Input Composer**
  - **Command Blocks**: Automatically organizes each command and its output into an independent block for 1-click copy, sanitized copy, in-block filtering, collapsing, and 1-click AI error diagnosis.
  - **Multi-Line Smart Composer**: Edit multi-line commands with mouse cursor positioning, autocomplete from snippets/history/remote paths, and search cross-session command history visually.
- **Real-Time Log Syntax Highlighting**
  - Automatically colors timestamps, `INFO / WARN / ERROR / FATAL` levels, Java class/line numbers, JSON keys, SQL keywords, URLs, and latencies without interfering with interactive apps like `vim`, `htop`, or `ls --color`.
- **Non-Blocking Live Log Filter Drawer (`TraceId` Focus View)**
  - Filter continuously streaming `tail -f` / `kubectl logs -f` output by `TraceId`, keyword, or regex with `±N` context lines and color-coded highlight chips — without ever pausing or breaking the live terminal stream.
- **Output Triggers**
  - Watch live terminal output to automatically apply custom highlights, send desktop notifications, or dispatch automated responses (with cooldown debouncing and optional confirmation gates).
- **8 Built-In Selection Formatters + Custom Formatter Studio**
  - Highlight any text in the terminal and right-click to instantly format & analyze:
    1. **JSON** pretty-printing;
    2. **SQL Formatting with `?` Parameter Binding** (reconstructs executable SQL from parameterized ORM/JDBC logs);
    3. **Java / K8S Stacktrace Cleanup** (highlights root cause and folds noisy framework frames);
    4. **Cron Expression Analyzer** (human-readable schedule + next 5 trigger times for 5-field Linux & 6-field Spring cron);
    5. **Unix Timestamp Converter** (seconds & milliseconds, local & UTC);
    6. **JWT Token Decoder** (Header/Payload inspection & expiration check);
    7. **URL Decoder & Query Parameter Table**;
    8. **Base64 Decoder / Encoder**.
  - **Custom Formatter Rules**: Create chained no-code formatting rules (such as unwrapping nested JSON or building `SQL IN (...)` lists) or connect local scripts directly to the right-click menu.
- **Side-by-Side Diff Inspector**
  - Set any selection as Baseline (Diff A) and compare side-by-side with Diff B, supporting **key-sorted JSON diff**, normalized SQL diff, and line-by-line text diff.
- **Sanitized Copy (`⌥⇧C` / `Alt+Shift+C`)**
  - Automatically masks phone numbers, ID numbers, emails, tokens, passwords, and internal IPs before copying to clipboard for safe sharing in team chats and tickets.
- **Parameterized Snippets & Built-In SRE Playbooks**
  - Supports `{{param}}` templates that auto-prefill from your current selection, plus built-in Java (CPU/Thread/GC), Linux (Network/Disk), and K8S diagnostic playbooks.

---

### 4. Built-In AI Ops Copilot

- **Multi-Model Support**: Built-in presets for **DeepSeek, Qwen, OpenAI, Zhipu GLM, and local Ollama**, plus any OpenAI-compatible private gateway and custom prompts; API keys are securely encrypted in your vault.
- **Automatic Error Detection & Stacktrace Diagnosis**: Detects failed commands and exception traces automatically, surfacing a quick banner for 1-click root-cause analysis and ready-to-run fix commands.
- **Natural Language to Shell**: Describe your goal in plain language to generate safe, accurate Linux/K8S commands ready to insert and execute.
- **Pre-Send Privacy Sanitization**: Optionally mask tokens, secrets, and sensitive data automatically before sending context to cloud models.

---

### 5. Native SQL / Redis Data Studio, File Transfer & Tunnels

- **Built-In SQL Studio**: Connect directly to **MySQL, PostgreSQL, and ClickHouse** — browse schemas, write queries in a syntax-highlighted editor, inspect results in a structured grid, jump to CLI, and enforce **Read-Only / Production Write Guardrails**.
- **Built-In Redis Studio**: Browse massive keyspaces via an auto-grouped **Namespace Tree**, inspect TTLs and types, edit values, and block accidental `FLUSHDB / FLUSHALL` commands.
- **Dual-Mode File Transfer**:
  - **SFTP Slide-Over Explorer**: Browse remote directories, upload local files, and download directly to your local Downloads folder.
  - **Bastion-Penetrating Pod Transfer**: Transfer files across multi-hop bastions into isolated K8S pods without direct SFTP access (supporting fast pipe transfer and `rz` / `sz` protocols), complete with live progress bar and cancel control.
- **Visual SSH Port Forwarding**: Manage and toggle `-L` (Local), `-R` (Remote), and `-D` (SOCKS5) SSH tunnels in one place.

---

### 6. Visual Personalization, Typography & Auto-Update

- **Custom Background Images & Frosted Blur**
  - Choose any local `.png / .jpg / .jpeg / .webp / .gif / .bmp` wallpaper with a **3%–100% live opacity slider + real-time terminal readability preview**, **frosted blur presets** (`0px / 4px / 10px / 20px`), 4 scaling modes (`Cover / Contain / Stretch / Center`), and **Global Immersive (frosted translucent cards)** vs **Terminal Only** scope.
- **Color Schemes & Day/Night Mode**: 20+ built-in themes, Light/Dark/System Auto switching, and a custom 16-color palette editor.
- **Precision Typography**: Primary & fallback fonts, ligatures, normal/bold font weights, cursor shape & blink, **automatic minimum contrast boost**, pixel line spacing, and crisp unified CJK rendering on Windows.
- **Bilingual UI & Built-In Auto-Update**: Switch instantaneously between English and 简体中文; built-in update checks, integrity verification, and 1-click in-place upgrades.

---

### 7. Enterprise Security, Audit & Encrypted Sync

- **Dual Secret Vault Modes (Your Choice)**
  - **OS Keychain (Default)**: Uses native macOS Keychain and Windows Credential Manager — zero plaintext passwords stored in configuration files.
  - **Local Encrypted Vault**: Master-password protected local encrypted vault with lock/unlock, password rotation, and optional OS Keychain auto-unlock.
- **Production Command Guardrail**: Intercepts dangerous commands (`rm -rf`, unqualified `DELETE / UPDATE`, `DROP TABLE`, `kubectl delete`, `FLUSHALL`, and custom rules) before execution with a mandatory confirmation dialog.
- **Session Recording & Command Audit Search**: Automatically archives `.log` transcripts and replayable `.cast` recordings, with cross-session command history search and automatic retention cleanup.
- **End-to-End Encrypted Backup & Multi-Backend Sync**: Export/import encrypted backup snapshots or sync across macOS and Windows via **GitHub Gist, GitLab Snippet, WebDAV (Nextcloud / Jianguoyun), iCloud / OneDrive shared folders, or a self-hosted sync server** with smart 3-way conflict merging.

---

## Keyboard Shortcuts

| Action | macOS | Windows |
| :--- | :--- | :--- |
| Global Command Palette (Hosts / Snippets / Themes / Actions) | `⇧⌘P` | `Ctrl+Shift+P` |
| Open / Return to Hosts Vault | `⌘K` | `Ctrl+Shift+K` |
| New Local Terminal Tab | `⌘T` | `Ctrl+Shift+T` |
| Close Active Pane / Tab | `⌘W` | `Ctrl+Shift+W` |
| Split Pane Right / Down | `⌘D` / `⇧⌘D` | `Ctrl+Shift+D` / `Ctrl+Shift+E` |
| Zoom / Restore Active Split Pane | `⇧⌘↵` | `Ctrl+Shift+↵` |
| Toggle Broadcast Input to All Panes | `⇧⌘I` | `Ctrl+Shift+I` |
| Find in Terminal Output | `⌘F` | `Ctrl+Shift+F` |
| Toggle Live Log Filter Drawer (`TraceId` View) | `⌘L` | `Ctrl+Shift+L` |
| Open AI Ops Copilot | `⌘I` | `Alt+I` |
| Format Selection (JSON / SQL / Stacktrace / Cron / etc.) | `⌥⇧F` | `Alt+Shift+F` |
| Sanitized Copy (Mask PII / Tokens) | `⌥⇧C` | `Alt+Shift+C` |
| Toggle Line Wrap / Horizontal Scroll | `⌥Z` | `Alt+Z` |
| Export Screen Log (`.log`) | `⌘S` | `Ctrl+Shift+S` |
| Zoom Font In / Out / Reset | `⌘+` / `⌘-` / `⌘0` | `Ctrl++` / `Ctrl+-` / `Ctrl+0` |
| Open Settings Center | `⌘,` | `Ctrl+,` |

---

## 8. `wuji` CLI & Self-Hosted Sync Server

Alongside the desktop app, WujiTerm includes standalone companion tools for automation and private team sync:

- **`wuji` CLI**: Manage hosts, encrypted secrets, triggers, snippets, port-forwarding tunnels, and cloud sync from the command line, or verify login automation pipelines headlessly:
  ```bash
  wuji host list
  wuji host add --name "Order Service Pod" --via bastion-k8s --step "shell->hlog"
  wuji verify --profile prod-order-pod
  wuji sync push
  ```
- **`wuji-sync-server`**: Lightweight self-hosted sync server for private intranet deployment, enabling fully self-sovereign encrypted sync across macOS and Windows workstations.

---

## Download & Installation

Download the latest release for your platform from the [Releases Page](https://github.com/CoolwjSoft/wuji-term/releases):

- **macOS (Universal — Apple Silicon M1/M2/M3/M4 & Intel)**:
  - Download `WujiTerm-<version>-macos-universal.dmg`, open it, and drag `WujiTerm.app` into `Applications`.
- **Windows 10 / 11 (`x86_64` Portable)**:
  - Desktop App: Download `WujiTerm-windows-x86_64.zip`, extract anywhere, and launch `wujiterm.exe`.
  - CLI & Private Sync Tools: Download `WujiTerm-cli-tools-windows-x86_64.zip` (`wuji.exe` + `wuji-sync-server.exe`).

---

## License

Licensed under the [MIT License](https://opensource.org/licenses/MIT). Issues, feature requests, and feedback are warmly welcome!
