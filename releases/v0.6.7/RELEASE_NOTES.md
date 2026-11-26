# WujiTerm v0.6.7

## 核心更新 / Highlights

- **版本更新说明 Markdown 富文本渲染**：自动更新页面中的版本新增功能说明现已支持完整 Markdown 格式渲染（标题、**粗体**、`行内代码`、有序/无序列表、引用块、代码块、分割线与表格）。
- **全平台同步发布（macOS / Linux x86_64 & ARM64 / Windows）**：提供 macOS Universal2、Linux `x86_64` / `aarch64` 与 Windows `x86_64` 完整构建产物。

---

## 下载与校验 / Downloads & SHA-256

| 平台 / Platform | 安装包 / Package | 大小 / Size | SHA-256 |
| :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1–M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.7-macos-universal.dmg` | 34.2 MB | `e4796c7670d9e1b9bd45ee4defe77dc49c0b0b017a7f24a566bc0aa3ca9ca92d` |
| **Linux (`x86_64`)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-x86_64.tar.gz` | 19.8 MB | `d3438976b6f9701f6a18ed3aed4b140de35f4b01f80be131fe907b31bc698792` |
| **Linux (`x86_64`)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-x86_64.tar.gz` | 5.8 MB | `12bfd4a0d3c18c7ec49f176acae36e319ee04b13e0f9a1c77597ec3c3c894c5f` |
| **Linux (`aarch64` / ARM64)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-aarch64.tar.gz` | 18.7 MB | `9a9cf3ba885a406c465d3f51552ade02e7c4f29064b30b43e1a5913fb564f7e3` |
| **Linux (`aarch64` / ARM64)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-aarch64.tar.gz` | 5.5 MB | `3e67ce1ea1e0c7788d08beee1c06139e593f285e3ecf93dbcc141c4bd7ce2af1` |
| **Windows 10/11 x86_64** (桌面便携版 / Desktop Portable) | `WujiTerm-windows-x86_64.zip` | 12.3 MB | `7c72d08605b36fa37c27eeecf9866083773a611baca95fac69642a460b998f52` |
| **Windows 10/11 x86_64** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.7 MB | `b6fb360bb7b4cea810c35796df09a1952f51a9ef8a18e30d916c6b321f5d5795` |

### 安装说明 / Installation
- **macOS**：打开 `.dmg` 并将 `WujiTerm.app` 拖入 `Applications` 文件夹即可使用（内含 `wuji` CLI 与 `wuji-sync-server`）。
- **Linux (`x86_64` / `aarch64`)**：解压对应安装包后运行 `./install.sh`（默认安装至 `~/.local/bin` 并注册桌面应用图标），或直接运行 `bin/wujiterm`。
- **Windows**：解压 `.zip` 至任意目录，双击运行 `wujiterm.exe`（绿色免安装，无需管理员权限；首次运行如遇 SmartScreen 提示，点击「更多信息」→「仍要运行」）。
