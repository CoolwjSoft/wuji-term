<div align="center">

<img src="docs/images/logo.png" width="128" height="128" alt="WujiTerm Logo" />

# WujiTerm

**Next-Generation High-Performance Smart Terminal & All-in-One Engineering Workbench for Developers, DevOps & SREs**

*Unifying SSH Terminal, Multi-Hop Bastion Automation, Live Kubernetes Log Diagnostics, Built-In System Monitor, Command Blocks, AI Ops Copilot, SQL & Redis Data Studio, Native Windows RDP / Cross-Platform VNC Desktop, Zero-Root Userspace VPN, SFTP/Pod File Transfer, and End-to-End Encrypted Cloud Sync in one fast native desktop app*

[![Release](https://img.shields.io/badge/Release-v0.6.0-F59E0B?style=flat-square)](https://github.com/smxj1314/wuji-term/releases/tag/v0.6.0)
[![Platform](https://img.shields.io/badge/Platform-macOS%20Universal%20%7C%20Windows%20x86__64-0EA5E9?style=flat-square)](https://github.com/smxj1314/wuji-term/releases/latest)
[![Experience](https://img.shields.io/badge/Experience-Native%20Speed%20%7C%20Fluid%20Rendering-10B981?style=flat-square)](#why-wujiterm)
[![Security](https://img.shields.io/badge/Security-OS%20Keychain%20%7C%20Local%20Encrypted%20Vault-6366F1?style=flat-square)](#9-enterprise-security-audit--encrypted-sync)
[![License](https://img.shields.io/badge/License-MIT-64748B?style=flat-square)](#license)

**[简体中文](README.md)** | **English**

[Why WujiTerm](#why-wujiterm) · [Visual Tour](#visual-tour) · [Full Feature Breakdown](#full-feature-breakdown) · [Shortcuts](#keyboard-shortcuts) · [CLI & Private Sync](#10-wuji-cli--self-hosted-sync-server) · [Installation](#download--installation)

</div>

---

## Why WujiTerm?

During real-world development and production troubleshooting, engineers constantly switch between **SSH terminals, jump-host login scripts, log viewers, online JSON/SQL formatters, diff tools, database clients, Redis browsers, RDP/VNC remote desktop apps, corporate VPN clients, SFTP tools, and AI chat tabs**. Fragmented tools break focus, while bloated terminal apps often lag and consume heavy memory under high-throughput log streams.

**WujiTerm** is a fast, lightweight native desktop terminal and all-in-one engineering workbench designed for developers, DevOps, and SREs — launching instantaneously, staying butter-smooth under massive log output, and unifying daily terminal sessions, log diagnostics, live system monitoring, database queries, Windows/VNC remote desktops, on-demand VPN tunneling, file transfers, and AI assistance inside one clean workspace:

| Scenario | Traditional Fragmented Tools | WujiTerm |
| :--- | :--- | :--- |
| **Heavy Log Throughput** | Stutters, drops frames, high memory & battery drain | **Hardware-accelerated native rendering**, ultra-smooth on massive logs, minimal idle footprint |
| **Multi-Hop Bastion & K8S** | Manual node selection, repeated passwords, shifting Pod IDs | **Reusable Jump Host inheritance + Visual Auto-Login + Smart Running Pod selector** |
| **Log Diagnostics & Monitoring** | Manual scrolling, stream-breaking `grep`, missing `htop` on containers | **Log highlight + non-blocking `TraceId` Live Filter + 8 formatters + Diff + Built-in Visual `htop` Monitor** |
| **Modern Terminal Ergonomics** | Hard to edit long commands or isolate command outputs | **Command Blocks + Multi-line Smart Composer + Custom Keybindings + Cross-Session Visual History** |
| **Database & File Ops** | Separate SQL / Redis / SFTP / `rz/sz` apps | **Built-in MySQL / PG / SQL Server / ClickHouse / Redis Studio + SFTP & Bastion-penetrating Pod Transfer** |
| **Windows & VNC Desktops** | Separate RDP / VNC apps, manual tunneling, painful file copies | **Embedded RDP & Cross-Platform VNC tabs + Encrypted WinRM Terminal + Shared Drive & Clipboard File Transfer** |
| **Corporate Intranet VPN** | OS VPN hijacks global routing, breaks local proxy, needs admin rights | **Zero-Root Userspace L2TP / IPSec VPN + Local SOCKS5 Proxy + On-Demand Per-Host Tunneling** |
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
> Connect directly to MySQL, PostgreSQL, SQL Server, ClickHouse, and Redis inside the same tab strip (with Read-Only Guardrails & Redis namespace tree), paired with the SFTP & bastion-penetrating Pod file transfer slide-over drawer.

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
- **System Status Bar & Tray Quick Switcher**
  - Native adaptive monochrome menu bar icon on **macOS** and notification-area tray icon on **Windows** displaying live active connections across Terminals, Databases, RDP/VNC Desktops, VPNs, and Port Forwards. Click to jump straight to any session, disconnect cleanly, or spawn a local terminal — toggleable live in Settings with zero restart.
- **Flexible Tab Management, Density Modes & Customizable Toolbar**
  - **3 Tab Bar Layout Modes + Dual Density**: (1) Single-row horizontal scroll; (2) Trailing `▾ More (N)` overflow dropdown (automatically keeps the active session visible); (3) Automatic multi-row wrap; paired with **Spacious** and **Compact** tab density modes.
  - **Tab Pinning & Drag-to-Reorder**: Pin critical production sessions to prevent accidental closure, drag tabs to reorder, and right-click to close other or right-side unpinned tabs.
  - **Dual-Action `+` Button**: Left-click defaults to opening a Local Terminal and can be configured (in Interface Settings or right from the popover) to launch any specific host from your Vault; **right-click `+` anytime to open a searchable Host List** for 1-click connection or setting a new left-click default.
  - **Customizable Toolbar & Status Footer**: Switch action buttons between **Icon Only / Text Only / Icon + Text**, and individually toggle top toolbar buttons (Command Palette, Split Panes, Command Blocks, Live Filter, System Monitor, AI Copilot, Line Wrap, Log Highlight, Snippets, Search, Files, Pod Transfer) as well as bottom footer indicators (dimensions, line wrap, font size, highlight state, host endpoint).
- **Long-Line Log Modes & Precision Mouse Ergonomics**
  - **Line Wrap / Single-Line Horizontal Scroll (`⌥Z` / `Alt+Z`)**: Single-line mode provides a smooth bottom scrollbar, trackpad horizontal swipe, and `Shift + Wheel` scrolling to read long JSON payloads and stack traces without line breaks.
  - **IDE-Grade Mouse Controls**: Click anywhere on the command line to position the shell cursor accurately (supporting mixed CJK and wrapped lines); double-click to select words, triple-click to select lines, optional copy-on-select, and `⌘/Ctrl + Click` to open URLs directly in your browser.
- **Arbitrary Split Panes, Pane Zoom & Broadcast Input**
  - Nested horizontal/vertical splits, quick pane focus cycling, temporary single-pane Zoom (`⇧⌘↵` / `Ctrl+Shift+↵`), and multi-pane **Broadcast Input (`⇧⌘I` / `Ctrl+Shift+I`)** to type once and execute across multiple cluster nodes simultaneously.
- **Global Command Palette, Custom Context Menu & Visual Keybinding Editor**
  - Keyboard-first Command Palette (`⌘P` / `Ctrl+Shift+P`) with fuzzy search across all hosts, Windows/VNC desktops, VPNs, databases, Redis caches, snippets, diagnostic playbooks, color schemes, and actions.
  - Fully editable terminal right-click menu (add/remove items, reorder, insert separators, bind custom command shortcuts).
  - **Full Visual Keybindings Center**: Customize all 27 shortcuts across 5 categories with live chord recording, automatic conflict detection & override prompts, individual disable, and 1-click reset.

---

### 2. Hosts Vault & Multi-Hop Bastion / Kubernetes Automation

- **All Connection Assets in One Place**
  - Manage **SSH remote hosts, Bastion/Jump hosts, automated login pipelines, Local Shells (auto-discovered OS shells), Windows Servers (RDP / WinRM / OpenSSH), Cross-Platform VNC Desktops, MySQL / PostgreSQL / SQL Server / ClickHouse databases, Redis caches, and Userspace VPN profiles**, plus automatic local SSH config discovery.
- **Reusable Jump Host Inheritance & On-Demand VPN Chaining**
  - Mark any Bastion or Jump Host as **"Reusable as Jump Host"** so downstream servers and Kubernetes pods inherit its credentials, encrypted password, and pre-login steps with one click — supporting both **in-session Relay jump** and **SSH `-J` tunnel jump** modes.
  - Bind any SSH, Local Terminal, Windows/VNC, or Database host to a **Userspace VPN profile** (and optionally stack an SSH bastion on top for dual-layer penetration) — clicking the host card dials the VPN and connects automatically.
- **Visual Auto-Login Pipelines & Smart Running Pod Selection**
  - Visually configure post-login jumps, menu selections, optional **pre-send step delays** (e.g., `1000ms`), and startup commands (such as entering a target pod and tailing logs) without writing fragile shell scripts.
  - **Dynamic `auto:service|fallback` Pod Matcher**: Automatically parses interactive bastion/K8S menus and prefers healthy `Running` pods by service name — unaffected when pod indices shift after deployments.
  - **Universal Prompt Detection & Snippet Integration**: Simply type `shell` to match macOS, Linux, and Windows shell prompts automatically, or `now` for immediate dispatch; pick commands straight from your Snippets library.
- **Flexible Views, Nested Groups & Full Manual Reordering**
  - Switch between **Grid Cards** and **Compact List** views with 5 sort modes (Custom order with `↑/↓`, Name A→Z / Z→A, Address, Protocol), collapsible Vault sidebar, nested folder groups (e.g. `Prod/OrderService`) with inline rename and persisted collapse state.
  - **Manual Reordering for Sidebar Assets & Host Groups**: Reorder both "Connection Assets" and "Host Groups" by **press-and-hold dragging**, toggling **`⇅ Sort` inline `↑/↓` buttons**, or using **right-click menus** (Move Up/Down/Top/Bottom); group order syncs across the entire Hosts Vault.
- **Production Safety & Reliability**
  - Host-level **`PROD` warning badges**, **Auto-Reconnect** with countdown & cancel, **Anti-Idle Heartbeat** to prevent bastion disconnects, and configurable **Launch Behavior** (Hosts Vault / Local Terminal / Specific Host).

---

### 3. Developer & SRE Diagnostics Workbench

- **Smart Terminal: Command Blocks & Multi-Line Input Composer**
  - **Command Blocks**: Automatically organizes each command and its output into an independent block for 1-click copy, sanitized copy, in-block filtering, collapsing, and 1-click AI error diagnosis.
  - **Multi-Line Smart Composer**: Edit multi-line commands with mouse cursor positioning, autocomplete from snippets/history/remote paths, and search cross-session command history visually (`⌘R` / `Ctrl+Shift+R`).
- **Built-In Live System Monitor Drawer (Visual `htop`)**
  - Toggle (`⇧⌘M` / `Ctrl+Shift+M`) a live telemetry drawer for either the remote SSH host or your local machine: real-time **CPU history sparkline, Memory & Swap gauges, load averages & uptime, disk mount usage, and a sortable/filterable Process Table (CPU / Mem / PID) with confirmation-gated process termination (`Kill`)**.
  - When `htop` is missing on minimal servers or containers, WujiTerm automatically surfaces a banner to launch a **zero-dependency, zero-disk-write colored built-in `htop` monitor** directly inside the terminal (compatible with Ubuntu, CentOS, Alpine, K8S Pods, and macOS).
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
  - Supports `{{param:default}}` templates that auto-prefill from your current selection, plus built-in Java (CPU/Thread/GC), Linux (Network/Disk), and K8S diagnostic playbooks.

---

### 4. Built-In AI Ops Copilot

- **Multi-Model Support**: Built-in presets for **DeepSeek, Qwen, OpenAI, Zhipu GLM, and local Ollama**, plus any OpenAI-compatible private gateway and custom prompts; API keys are securely encrypted in your vault.
- **Automatic Error Detection & Stacktrace Diagnosis**: Detects failed commands and exception traces automatically, surfacing a quick banner for 1-click root-cause analysis and ready-to-run fix commands.
- **Natural Language to Shell**: Describe your goal in plain language to generate safe, accurate Linux/K8S commands ready to insert and execute.
- **Pre-Send Privacy Sanitization**: Optionally mask tokens, secrets, and sensitive data automatically before sending context to cloud models.

---

### 5. Native SQL / Redis Data Studio, File Transfer & Tunnels

- **Built-In Multi-Engine SQL Studio**: Connect directly to **MySQL, PostgreSQL, SQL Server (MSSQL `1433`), and ClickHouse** — browse schemas, write queries in a syntax-highlighted editor, inspect results in a structured grid with JSON cell pretty-viewing, **export query results to CSV / JSON**, run session/storage diagnostics, jump to CLI, and enforce **Read-Only / Production Write Guardrails**; supports **SSH Bastion & Userspace VPN tunneling**.
- **Built-In Redis Studio**: Browse massive keyspaces via an auto-grouped **Namespace Tree**, inspect TTLs and types, edit values, run interactive Redis commands, block accidental `FLUSHDB / FLUSHALL` commands, and connect through SSH Bastions or VPNs.
- **Dual-Mode File Transfer**:
  - **SFTP Slide-Over Explorer**: Browse remote directories (including Windows drive trees), upload local files, and download directly to your local Downloads folder.
  - **Bastion-Penetrating Pod Transfer**: Transfer files across multi-hop bastions into isolated K8S pods without direct SFTP access (supporting fast pipe transfer and `rz` / `sz` protocols), complete with live progress bar and cancel control.
- **Visual SSH Port Forwarding**: Manage and toggle `-L` (Local), `-R` (Remote), and `-D` (SOCKS5) SSH tunnels in one place.

---

### 6. Native Windows Server Ops & Cross-Platform VNC Remote Desktop

- **Embedded Native RDP Remote Desktop Tabs (`3389`)**
  - Interact with Windows Remote Desktops directly inside WujiTerm's tab strip — full **CredSSP (NLA) & Active Directory domain login**, **dynamic auto-resize or fixed resolution**, 1-click `Ctrl+Alt+Del`, bidirectional clipboard sync, and **View-Only mode** for safe observation.
  - **Zero-Extra-Port Bidirectional File Transfer**:
    - **Direct Clipboard Copy-Paste & Drag-Drop**: Push local files to the remote clipboard and press `Ctrl+V` in remote Explorer, or copy files (`Ctrl+C`) on the remote desktop and download them straight to your machine with live progress tracking.
    - **Mounted Shared Drive (`\\tsclient\WujiShare`)**: Expose a local folder directly inside remote "This PC" for instant two-way file sharing.
- **Cross-Platform VNC Remote Desktop (`5900+` or `:N` Display)**
  - Native support for **Linux (TigerVNC / x11vnc), Windows (TightVNC / UltraVNC / RealVNC), QEMU/KVM hypervisor consoles, and macOS Screen Sharing (ARD)** — featuring responsive scaling, shared sessions, bidirectional clipboard sync, and View-Only mode.
- **Agentless Encrypted WinRM Terminal (`5985` / `5986`)**
  - Connects directly to remote PowerShell / CMD over NTLM-sealed encrypted sessions (works out of the box with Windows Server's default `AllowUnencrypted=false` policy) inside the native GPU terminal — zero third-party agents required.
- **Windows OpenSSH Enhancements & Full Tunnel Chaining**
  - Switch default shell between PowerShell, `pwsh`, and CMD, browse multi-drive Windows trees (`C:\`, `D:\`) with SCP / WinRM bidirectional file transfer, and route **RDP, VNC, WinRM, and Windows OpenSSH** seamlessly through **SSH Bastions and/or Userspace VPNs**.

---

### 7. Zero-Root Userspace VPN & On-Demand Asset Penetration

- **No Admin Privileges · Zero Global Routing Pollution**
  - Runs completely in userspace without modifying OS network interfaces or global routing tables — **connect to your corporate VPN without disrupting local internet traffic or proxy split-routing rules**.
  - Supports **L2TP** and **L2TP over IPSec (Pre-Shared Key)** with PAP / CHAP / MS-CHAPv2 authentication, automatic **auth-failure circuit breaker** to prevent corporate account lockouts, and a **direct DNS resolver** that bypasses local Fake-IP proxy pollution.
- **Full-Screen Live VPN Workbench Tab**
  - Opens a dedicated top-bar tab showing **local SOCKS5 address, assigned intranet IP & gateway, uptime, real-time TX/RX traffic counters**, and a searchable/filterable connection & forwarding log console. Closing the tab disconnects cleanly.
- **Local SOCKS5 Proxy + 1-Click Per-Host Routing**
  - Exposes a local `SOCKS5` proxy (default `127.0.0.1:1080`) with 1-click copy for proxy address or shell `export` variables and a 1-click proxy-injected Local Terminal — ready for browsers, rule-based proxy apps, or `curl`.
  - Link any **SSH, Local Terminal, Windows (RDP / VNC / WinRM / OpenSSH), or Database (MySQL / PostgreSQL / SQL Server / ClickHouse / Redis)** host to auto-dial and route through the VPN on demand (even stacked with an SSH Bastion for dual-layer access).

---

### 8. Visual Personalization, Typography & Auto-Update

- **Custom Background Images & Frosted Blur**
  - Choose any local `.png / .jpg / .jpeg / .webp / .gif / .bmp` wallpaper with a **3%–100% live opacity slider + real-time terminal readability preview**, **frosted blur presets** (`0px / 4px / 10px / 20px`), 4 scaling modes (`Cover / Contain / Stretch / Center`), and **Global Immersive (frosted translucent cards)** vs **Terminal Only** scope.
- **Color Schemes & Day/Night Mode**: 20+ built-in themes, Light/Dark/System Auto switching, and a custom 16-color palette editor.
- **Precision Typography**: Primary & fallback fonts, ligatures, normal/bold font weights, cursor shape & blink, **automatic minimum contrast boost**, pixel line spacing, and crisp unified CJK rendering on Windows.
- **Bilingual UI & Built-In Auto-Update**: Switch instantaneously between English and 简体中文; built-in update checks, integrity verification, and 1-click in-place upgrades.

---

### 9. Enterprise Security, Audit & Encrypted Sync

- **Dual Secret Vault Modes (Your Choice)**
  - **OS Keychain (Default)**: Uses native macOS Keychain and Windows Credential Manager to store all passwords, VPN pre-shared keys, and API keys — zero plaintext secrets in configuration files.
  - **Local Encrypted Vault**: Master-password protected local encrypted vault with lock/unlock, password rotation, and optional OS Keychain auto-unlock.
- **Production Command Guardrail**: Intercepts dangerous commands (`rm -rf`, unqualified `DELETE / UPDATE`, `DROP TABLE`, `kubectl delete`, `FLUSHALL`, and custom rules) before execution with a mandatory confirmation dialog.
- **Session Recording & Command Audit Search**: Automatically archives `.log` transcripts and replayable `.cast` recordings, with cross-session command history search and automatic retention cleanup.
- **End-to-End Encrypted Backup & Multi-Backend Sync**: Export/import encrypted backup snapshots (covering SSH, Windows/VNC, Databases, VPNs, and automation workflows) or sync across macOS and Windows via **GitHub Gist, GitLab Snippet, WebDAV (Nextcloud / Jianguoyun), iCloud / OneDrive shared folders, or a self-hosted sync server** with smart 3-way conflict merging.

---

## Keyboard Shortcuts

> All 27 core shortcuts can be visually recorded, customized, disabled, or reset in **Settings → Keybindings**.

| Action | macOS Default | Windows Default |
| :--- | :--- | :--- |
| Global Command Palette (Hosts / Snippets / Themes / Actions) | `⌘P` | `Ctrl+Shift+P` |
| Open / Return to Hosts Vault | `⌘K` | `Ctrl+Shift+K` |
| New Local Terminal Tab | `⌘T` | `Ctrl+Shift+T` |
| Close Active Pane / Tab | `⌘W` | `Ctrl+Shift+W` |
| Split Pane Right / Down | `⌘D` / `⇧⌘D` | `Ctrl+Shift+D` / `Ctrl+Shift+E` |
| Focus Previous / Next Split Pane | `⌘[` / `⌘]` | `Ctrl+Shift+[` / `Ctrl+Shift+]` |
| Zoom / Restore Active Split Pane | `⇧⌘↵` | `Ctrl+Shift+↵` |
| Toggle Broadcast Input to All Panes | `⇧⌘I` | `Ctrl+Shift+I` |
| Find in Terminal Output | `⌘F` | `Ctrl+Shift+F` |
| Toggle Live Log Filter Drawer (`TraceId` View) | `⌘L` | `Ctrl+Shift+L` |
| Toggle Live System Monitor (Built-In `htop`) | `⇧⌘M` | `Ctrl+Shift+M` |
| Cross-Session Visual Command History Search | `⌘R` | `Ctrl+Shift+R` |
| Toggle Command Blocks View | `⇧⌘B` | `Ctrl+Shift+B` |
| Open AI Ops Copilot | `⌘I` | `Alt+I` |
| Format Selection (JSON / SQL / Stacktrace / Cron / etc.) | `⌥⇧F` | `Alt+Shift+F` |
| Sanitized Copy (Mask PII / Tokens) | `⌥⇧C` | `Alt+Shift+C` |
| Toggle Line Wrap / Horizontal Scroll | `⌥Z` | `Alt+Z` |
| Export Screen Log (`.log`) | `⌘S` | `Ctrl+Shift+S` |
| Zoom Font In / Out / Reset | `⌘=` / `⌘-` / `⌘0` | `Ctrl+Shift+=` / `Ctrl+Shift+-` / `Ctrl+0` |
| Open Settings Center | `⌘,` | `Ctrl+,` |

---

## 10. `wuji` CLI & Self-Hosted Sync Server

Alongside the desktop app, WujiTerm includes an AI-friendly declarative CLI (changes hot-reload directly into open GUI windows) and a lightweight private sync server:

- **`wuji` CLI**: Manage SSH hosts, multi-hop automation pipelines, Windows (RDP/WinRM/OpenSSH), VNC, Databases (MySQL/PG/SQL Server/ClickHouse/Redis), Userspace VPNs, encrypted secrets, triggers, snippets, port-forwarding tunnels, atomic JSON batch apply (`wuji apply`), and cloud sync — plus closed-loop headless verification:
  ```bash
  # Configure & headlessly verify SSH / Bastion / K8S automation pipelines
  wuji host list
  wuji host upsert --name "Order Service Pod" --via bastion-k8s --step "Pod>=>auto:order" --step "shell=>hlog"
  wuji host verify bastion-k8s --timeout-secs 25

  # Configure & verify Userspace VPN, Windows RDP/WinRM, VNC & SQL/Redis hosts
  wuji vpn upsert --id corp-vpn --type l2tp-ipsec --server vpn.example.com --user ops --socks-port 1080
  wuji vpn verify corp-vpn
  wuji win ping win-ad-rdp
  wuji vnc ping kvm-console-01
  wuji db query prod-erp-mssql "SELECT TOP 10 name FROM sys.databases"

  # Trigger encrypted cloud sync or open GUI directly into any asset
  wuji sync push
  wuji open --host win-ad-rdp
  ```
- **`wuji-sync-server`**: Lightweight self-hosted sync server for private intranet deployment, enabling fully self-sovereign encrypted sync across macOS and Windows workstations.

---

## Download & Installation

Latest Release: **`v0.6.0`** — download installers from [GitHub Releases (`v0.6.0`)](https://github.com/smxj1314/wuji-term/releases/tag/v0.6.0) or directly from the repository folder [releases/v0.6.0](releases/v0.6.0):

| Platform & Architecture | Package | Size | GitHub Release | Repo Direct |
| :--- | :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1/M2/M3/M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.0-macos-universal.dmg` | 31.6 MB | [Download](https://github.com/smxj1314/wuji-term/releases/download/v0.6.0/WujiTerm-0.6.0-macos-universal.dmg) | [Direct](releases/v0.6.0/WujiTerm-0.6.0-macos-universal.dmg) |
| **Windows 10 / 11 (`x86_64`)** Portable Desktop App | `WujiTerm-windows-x86_64.zip` | 10.7 MB | [Download](https://github.com/smxj1314/wuji-term/releases/download/v0.6.0/WujiTerm-windows-x86_64.zip) | [Direct](releases/v0.6.0/WujiTerm-windows-x86_64.zip) |
| **Windows 10 / 11 (`x86_64`)** CLI & Private Sync Server (`wuji` + `wuji-sync-server`) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.1 MB | [Download](https://github.com/smxj1314/wuji-term/releases/download/v0.6.0/WujiTerm-cli-tools-windows-x86_64.zip) | [Direct](releases/v0.6.0/WujiTerm-cli-tools-windows-x86_64.zip) |

### Installation Notes
- **macOS (Universal — Apple Silicon M1/M2/M3/M4 & Intel)**:
  - Download `WujiTerm-0.6.0-macos-universal.dmg`, open it, and drag `WujiTerm.app` into `Applications` (bundles `wuji` CLI and `wuji-sync-server` inside the app).
- **Windows 10 / 11 (`x86_64` Portable)**:
  - Desktop App: Download `WujiTerm-windows-x86_64.zip`, extract to any folder (e.g. `D:\Apps\WujiTerm`), and launch `wujiterm.exe` (no installation or admin privileges required; if SmartScreen appears on first launch, click **More info → Run anyway**).
  - CLI & Private Sync Tools: Download `WujiTerm-cli-tools-windows-x86_64.zip` (`wuji.exe` + `wuji-sync-server.exe`).
- **SHA-256 Checksums** ([SHA256SUMS.txt](releases/v0.6.0/SHA256SUMS.txt)):
  - `WujiTerm-0.6.0-macos-universal.dmg`: `2d7d656dc5c740d39285baaea42fa98c8c2b1d829ffbe9ec6a844dc76b1bf6fc`
  - `WujiTerm-windows-x86_64.zip`: `975fa92af6c79fdad532699022fba2495dd6fd0d853bdaf861ae1b6bf3c78010`
  - `WujiTerm-cli-tools-windows-x86_64.zip`: `9b9dda477c9207e382a3d2f92b1ce1b5a0c6f2254446d7f315a0a83aa56c9622`
- **Built-In Auto-Update Feed**:
  - Point **Settings → Updates** to `https://raw.githubusercontent.com/smxj1314/wuji-term/main/releases/latest.json` (or `https://api.github.com/repos/smxj1314/wuji-term/releases/latest`).

---

## License

Licensed under the [MIT License](https://opensource.org/licenses/MIT). Issues, feature requests, and feedback are warmly welcome!
