# WujiTerm v0.6.2

## 核心更新 / Highlights

- **全平台同步发布（macOS / Linux / Windows）**：正式提供 macOS Universal2、Linux `x86_64` 与 Windows `x86_64` 三端完整构建产物。
- **Linux 桌面集成与自动更新增强**：提供 `.desktop` 桌面入口、应用图标、`install.sh` 一键安装脚本，并优化应用内自动更新的架构匹配。
- **Windows 托盘菜单修复与稳定性提升**：修复 Windows 状态栏/托盘右键菜单构建问题并提升整体稳定性。

---

## 下载与校验 / Downloads & SHA-256

| 平台 / Platform | 安装包 / Package | 大小 / Size | SHA-256 |
| :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1–M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.2-macos-universal.dmg` | 31.6 MB | `0397f2b91ab7216b879bd6c9679a9eafb55a0c7a803a59fef62c9d3cbbe1c6f2` |
| **Linux (`x86_64`)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-x86_64.tar.gz` | 18.4 MB | `5057212845d643a66281fce2be4199af6278c84568d928a780cebc9251529019` |
| **Linux (`x86_64`)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-x86_64.tar.gz` | 5.6 MB | `9e13be5fd6daa62eb780ff1b91e1e7589f26fdbab5e97c330` |
| **Windows 10/11 x86_64** (桌面便携版 / Desktop Portable) | `WujiTerm-windows-x86_64.zip` | 11.1 MB | `f021202e862cd5270b982da861bc04f9b07b446ab154d326e0c7faa246e87792` |
| **Windows 10/11 x86_64** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.5 MB | `509d84abfaf15a9664fe12b0087e8cb7231cb082bfe4f79decb0b79b1f083179` |

### 安装说明 / Installation
- **macOS**：打开 `.dmg` 并将 `WujiTerm.app` 拖入 `Applications` 文件夹即可使用（内含 `wuji` CLI 与 `wuji-sync-server`）。
- **Linux (`x86_64`)**：解压 `WujiTerm-linux-x86_64.tar.gz` 后运行 `./install.sh`（默认安装至 `~/.local/bin` 并注册桌面应用图标），或直接运行 `bin/wujiterm`。
- **Windows**：解压 `.zip` 至任意目录，双击运行 `wujiterm.exe`（绿色免安装，无需管理员权限；首次运行如遇 SmartScreen 提示，点击「更多信息」→「仍要运行」）。
