# WujiTerm v0.6.5

## 核心更新 / Highlights

- **终端内核与现代 VT 协议全面跃升**：
  - 升级 `libghostty-vt` 桥接与 GPU 渲染器：支持 32 字节 UTF-8 复合字素（Emoji / ZWJ / 变体选择符）、波浪线/双线/点线/虚线下划线及彩色下划线、删除线/上划线/弱化显示、完整 TUI 鼠标事件上报（含 `Shift` 穿透选词与备用屏滚轮）、Bracketed Paste（Mode 2004）与 Synchronized Output（Mode 2026）。
  - 新增 **OSC 52** 剪贴板写入、**OSC 8** 终端超链接（`Cmd/Ctrl+Click` 点击打开）、**OSC 9 / 777** 桌面通知、**OSC 133** 语义提示符跳转（`Cmd/Ctrl+Shift+Up/Down`）、**原生系统输入法光标跟随（IME Cursor Area）**，以及覆盖全量滚回缓冲区的终端历史搜索与高亮。
- **纯 Rust 原生 SSH/SFTP 与隧道升级**：
  - 引入 `russh` + `russh-sftp` 原生客户端，提供真实权限/大小/修改时间的 SFTP 目录浏览、64 KiB 分片上传下载、新建目录/重命名/删除/`chmod`，以及 **远程文件本地编辑自动监听保存并实时回传**。
  - 主机配置新增 **SSH 私钥路径（`identity_file`）** 选择与自动注入；端口转发升级支持密码认证原生本地（`-L`）/动态 SOCKS5（`-D`）隧道与 **指数退避自动重连**；内置 **ZMODEM（CRC-16/CRC-32 校验 + 流式分片限速）** 与 **`trzsz`（`tsz`/`trz`）** 终端内联文件传输。
- **数据库全引擎 TLS/SSL 与 VPN 企业内网增强**：
  - **MySQL / PostgreSQL / Redis / ClickHouse / SQL Server** 五大引擎全面支持 TLS/SSL 加密连接及证书校验开关（含 PostgreSQL RFC 5802 SCRAM-SHA-256 服务端签名真校验），同步支持 GUI 开关与 `wuji` CLI `--tls` / `--tls-insecure`。
  - 用户态 L2TP/IPSec VPN 新增 **PPP IPCP 内网 DNS 自动协商与隧道内 UDP DNS 解析**，以及 **IPSec Phase 2 SA 50 分钟自动重协商（Rekey）** 保障长连接不断流。
- **AI 运维副驾驶、录像可视化回放与工作区持久化**：
  - **AI 运维副驾驶**：新增实时 SSE 流式打字机输出、多轮对话上下文记忆，以及原生 **Anthropic Claude** 与 **Google Gemini** 接口协议适配。
  - **审计录像内置播放器**：审计工作台新增 Asciinema v2（`.cast`）原生可视化终端回放器，支持播放/暂停/进度拖动/`0.5x`–`4x` 倍速与空闲时长压缩。
  - **工作区会话持久化与多窗口**：自动保存/恢复窗口尺寸、标签页、嵌套分屏布局与工作目录，新增菜单「新建窗口（`--new-window`）」。
- **稳定性与全平台补齐**：
  - 修复格式化工具栏空胶囊按钮、补齐 Linux 本地系统监控（`/proc` + `df` + `ps`）、突破 WinRM 12 KB 文件上传限制（流式分片传输）、新增云同步删除墓碑（Tombstone）防止已删资产被旧端复活，并补齐 Linux `.tar.gz` 原子自更新重启与图形化文件选择器。

---

## 下载与校验 / Downloads & SHA-256

| 平台 / Platform | 安装包 / Package | 大小 / Size | SHA-256 |
| :--- | :--- | :--- | :--- |
| **macOS Universal** (Apple Silicon M1–M4 & Intel, macOS 13.0+) | `WujiTerm-0.6.5-macos-universal.dmg` | 33.7 MB | `c216273069d41b7a88fc77c601d7882d6fa3154e74b40f64f3f1da9f845ae4aa` |
| **Linux (`x86_64`)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-x86_64.tar.gz` | 19.5 MB | `6171dc9628bb4233d90b8ec7c02a1bbf8cf7b0ce2e7d42042452c41473c0e797` |
| **Linux (`x86_64`)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-x86_64.tar.gz` | 5.7 MB | `e293bd6b0eb24b4a02192a32cf7e2d2e5e13b90a4a39e9116b4d25950b3265af` |
| **Linux (`aarch64` / ARM64)** (桌面版 + CLI + 同步服务端) | `WujiTerm-linux-aarch64.tar.gz` | 18.4 MB | `acceadb9e82ae6cf2038bdf30e55cb7dfadd2a87aa03a479994ddb12de2a4cb7` |
| **Linux (`aarch64` / ARM64)** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-linux-aarch64.tar.gz` | 5.4 MB | `f20415d58766b4904df2d73b6f088009d364eb94072f12d847638d84ce8d6520` |
| **Windows 10/11 x86_64** (桌面便携版 / Desktop Portable) | `WujiTerm-windows-x86_64.zip` | 12.1 MB | `73a1d8598805de43de5bdc91f9c2eefe407c80a771287b3e9c96551511b018bb` |
| **Windows 10/11 x86_64** (CLI 与私有同步服务端 / CLI & Sync Server) | `WujiTerm-cli-tools-windows-x86_64.zip` | 5.6 MB | `135a8d4b7fa4b86b4bcce0c12b2c31821e16143fbc7d8a77cbacb9fc6c7e2bcc` |

### 安装说明 / Installation
- **macOS**：打开 `.dmg` 并将 `WujiTerm.app` 拖入 `Applications` 文件夹即可使用（内含 `wuji` CLI 与 `wuji-sync-server`）。
- **Linux (`x86_64` / `aarch64`)**：解压对应架构的 `.tar.gz` 后运行 `./install.sh`（默认安装至 `~/.local/bin` 并注册桌面应用图标），或直接运行 `bin/wujiterm`。
- **Windows**：解压 `.zip` 至任意目录，双击运行 `wujiterm.exe`（绿色免安装，无需管理员权限；首次运行如遇 SmartScreen 提示，点击「更多信息」→「仍要运行」）。
