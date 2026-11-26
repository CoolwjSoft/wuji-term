# WujiTerm v0.6.6

## 核心更新 / Highlights

- **自动更新策略三段式升级**：在「设置中心 → 版本管理与自动更新」中新增「发现新版本处理策略」，支持 **仅检查提示**、**检查并下载（默认）** 与 **自动下载并升级** 三种模式。
- **全平台同步发布（macOS / Linux x86_64 & ARM64 / Windows）**：提供 macOS Universal2、Linux `x86_64` / `aarch64` 与 Windows `x86_64` 完整构建产物。

---

## 下载与校验 / Downloads & SHA-256

| 平台 / Platform | 安装包 / Package | 大小 / Size | SHA-256 |
| :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1–M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.6-macos-universal.dmg` | 34.2 MB | `457625581985df6cfa6799857486337e0b7b1ed7478497bd37ef0217df625bd0` |
| **Linux (`x86_64`)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-x86_64.tar.gz` | 19.8 MB | `e5f1b3d415b61b890fdb06d6d003036e9496c09322a8f71596bc4a97b3fcd51d` |
| **Linux (`x86_64`)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-x86_64.tar.gz` | 5.8 MB | `90aed8eb8d11a93f3cd361ca6cfe985f2015b16b9e79faea516eb2bf21475c5a` |
| **Linux (`aarch64` / ARM64)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-aarch64.tar.gz` | 18.7 MB | `17e4dd5e4e5fbe3dfb348295c0ecf6106323dddaee8c771a82c8fc811932776b` |
| **Linux (`aarch64` / ARM64)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-aarch64.tar.gz` | 5.5 MB | `70ead7f2b645f7fe5c064ffe03af7cf5c15914edd8af2de0d8c8c103ce681b98` |
| **Windows 10/11 x86_64** (桌面便携版 / Desktop Portable) | `WujiTerm-windows-x86_64.zip` | 12.3 MB | `d52e36bde803d2f3edfe23995e157318a774a4d4003a04fc1c266577188993e1` |
| **Windows 10/11 x86_64** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.7 MB | `ea69a41da3a063f06d8172775c9607590f38999bcc9996e45eb28b19529a56ad` |

### 安装说明 / Installation
- **macOS**：打开 `.dmg` 并将 `WujiTerm.app` 拖入 `Applications` 文件夹即可使用（内含 `wuji` CLI 与 `wuji-sync-server`）。
- **Linux (`x86_64` / `aarch64`)**：解压对应安装包后运行 `./install.sh`（默认安装至 `~/.local/bin` 并注册桌面应用图标），或直接运行 `bin/wujiterm`。
- **Windows**：解压 `.zip` 至任意目录，双击运行 `wujiterm.exe`（绿色免安装，无需管理员权限；首次运行如遇 SmartScreen 提示，点击「更多信息」→「仍要运行」）。
