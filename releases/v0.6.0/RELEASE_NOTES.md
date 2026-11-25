# WujiTerm v0.6.0

## 核心更新亮点 / Highlights

- **Windows Server 原生运维 & 跨平台 VNC 远程桌面**
  - 标签页原生内嵌 **RDP 远程桌面 (`3389`)**：支持 CredSSP (NLA)、动态自适应分辨率、只读监看、`Ctrl+Alt+Del`、剪贴板/拖拽双向传文件与本机目录挂载共享盘 (`\\tsclient\WujiShare`)。
  - 原生兼容 **跨平台 VNC (`5900+` / `:N`)**（Linux TigerVNC/x11vnc、Windows TightVNC/UltraVNC/RealVNC、KVM/QEMU 与 macOS ARD）。
  - 新增 **WinRM 加密交互式终端 (`5985`/`5986`)** 与 **Windows OpenSSH 多盘符文件浏览器**，全协议支持 SSH 堡垒机与 VPN 隧道穿透。
- **免管理员权限 · 纯用户态内置 VPN 与按需穿透**
  - 无需管理员权限、不污染系统全局路由表，原生支持 **L2TP** 与 **L2TP over IPSec (PSK)**、鉴权失败自动熔断保护与直连 DNS（绕过 Fake-IP）。
  - 提供全屏 VPN 实时工作台标签页（内网 IP、实时流量、日志检索）、本地 `SOCKS5` 代理以及 SSH / Windows / VNC / 数据库全资产一键按需穿透。
- **SQL Server (MSSQL) & 数据工作台增强**
  - 原生支持 **MySQL / PostgreSQL / SQL Server (`1433`) / ClickHouse / Redis**，支持结果集一键导出 CSV / JSON、JSON 单元格美化与会话诊断。
- **内置实时系统监控（可视化 `htop`）、系统状态栏/托盘与全量快捷键自定义**
  - `⇧⌘M` / `Ctrl+Shift+M` 一键打开 CPU 曲线、内存/Swap、磁盘空间与进程管理抽屉，并在无 `htop` 容器中支持零依赖终端内置彩色 `htop`。
  - 新增 macOS 菜单栏模板图标与 Windows 系统托盘快速会话切换、标签页宽松/紧凑密度与 27 项快捷键实时录制。

---

## 下载与校验 / Downloads & SHA-256

| 平台 / Platform | 安装包 / Package | 大小 / Size | SHA-256 |
| :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1–M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.0-macos-universal.dmg` | 31.6 MB | `2d7d656dc5c740d39285baaea42fa98c8c2b1d829ffbe9ec6a844dc76b1bf6fc` |
| **Windows 10/11 x86_64** (桌面便携版 / Desktop Portable) | `WujiTerm-windows-x86_64.zip` | 10.7 MB | `975fa92af6c79fdad532699022fba2495dd6fd0d853bdaf861ae1b6bf3c78010` |
| **Windows 10/11 x86_64** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.1 MB | `9b9dda477c9207e382a3d2f92b1ce1b5a0c6f2254446d7f315a0a83aa56c9622` |

### 安装说明 / Installation
- **macOS**：打开 `.dmg` 并将 `WujiTerm.app` 拖入 `Applications` 文件夹即可使用（内含 `wuji` CLI 与 `wuji-sync-server`）。
- **Windows**：解压 `.zip` 至任意目录，双击运行 `wujiterm.exe`（绿色免安装，无需管理员权限；首次运行如遇 SmartScreen 提示，点击「更多信息」→「仍要运行」）。
