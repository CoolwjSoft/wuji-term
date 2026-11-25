# WujiTerm v0.6.1

## 核心更新 / Highlights

- **折叠/展开状态持久化**：左侧资产导航栏折叠状态与主机分组（含未分组）折叠/展开状态现已自动记录到 `config.toml`，重启或同步配置后自动恢复。
- **稳定性与细节优化**：优化 UI 交互与打包构建产物（macOS Universal2 & Windows x86_64）。

---

## 下载与校验 / Downloads & SHA-256

| 平台 / Platform | 安装包 / Package | 大小 / Size | SHA-256 |
| :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1–M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.1-macos-universal.dmg` | 31.6 MB | `7bca5b17db1ddae18488d47505c8ec6987018da43073db274fb7c827b5748698` |
| **Windows 10/11 x86_64** (桌面便携版 / Desktop Portable) | `WujiTerm-windows-x86_64.zip` | 11.1 MB | `46891e3a12d32433a3a9a2f50bdd456892c6d9af4560234271fa9b4d94240402` |
| **Windows 10/11 x86_64** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.5 MB | `5b3e5db233e7baa7115002161c482ff9870f2e0bf4174f33d26dc2366cdab5c1` |

### 安装说明 / Installation
- **macOS**：打开 `.dmg` 并将 `WujiTerm.app` 拖入 `Applications` 文件夹即可使用（内含 `wuji` CLI 与 `wuji-sync-server`）。
- **Windows**：解压 `.zip` 至任意目录，双击运行 `wujiterm.exe`（绿色免安装，无需管理员权限；首次运行如遇 SmartScreen 提示，点击「更多信息」→「仍要运行」）。
