# WujiTerm v0.6.4

## 核心更新 / Highlights

- **主机库安全与权限增强**：新增 `vault_security` 安全模块并集成命令面板与系统菜单入口。
- **修复 GitHub Releases 自动更新解析**：修正 `parse_update_manifest_for_keys` 优先匹配 `assets` 数组，避免误将 Release API 元数据 `url` 当作安装包下载，并增加非安装包内容拦截校验。
- **全平台同步发布（macOS / Linux / Windows）**：提供 macOS Universal2、Linux `x86_64` 与 Windows `x86_64` 三端完整构建产物。

---

## 下载与校验 / Downloads & SHA-256

| 平台 / Platform | 安装包 / Package | 大小 / Size | SHA-256 |
| :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1–M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.4-macos-universal.dmg` | 31.7 MB | `69c6a550167956310fbd890375deb24109c765da5e3b083bbe6b799b8005200b` |
| **Linux (`x86_64`)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-x86_64.tar.gz` | 18.4 MB | `3b988601bee94cb0321b27c78ac1d4cc86feb109cd619efbe897d24ee3dab265` |
| **Linux (`x86_64`)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-x86_64.tar.gz` | 5.6 MB | `af0e16bbd1ff38cabc0698430afc22a9973ef2b2ab746a2440960e6ebbae912c` |
| **Windows 10/11 x86_64** (桌面便携版 / Desktop Portable) | `WujiTerm-windows-x86_64.zip` | 11.2 MB | `0972380f578b539dee11ec0fb494ced4682ae5ceb7b7eef25e0da240fdb75a24` |
| **Windows 10/11 x86_64** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.5 MB | `b7b1f210c4719386177878c62273882bee6c90d39598f70014dc3ca216940115` |

### 安装说明 / Installation
- **macOS**：打开 `.dmg` 并将 `WujiTerm.app` 拖入 `Applications` 文件夹即可使用（内含 `wuji` CLI 与 `wuji-sync-server`）。
- **Linux (`x86_64`)**：解压 `WujiTerm-linux-x86_64.tar.gz` 后运行 `./install.sh`（默认安装至 `~/.local/bin` 并注册桌面应用图标），或直接运行 `bin/wujiterm`。
- **Windows**：解压 `.zip` 至任意目录，双击运行 `wujiterm.exe`（绿色免安装，无需管理员权限；首次运行如遇 SmartScreen 提示，点击「更多信息」→「仍要运行」）。
