# WujiTerm v0.6.18

## 新增功能
- **远程桌面（WebRTC + H.264）**：新增 `wuji-remote-desktop` 与 WebRTC 桌面串流能力（支持 macOS ScreenCaptureKit、Windows 与 Linux），配备桌面控制界面与 Web 控制端（`desktop.html`），并支持 Cloudflare 信令部署。
- **终端输出代码位置跳转（Code Jump）**：支持 `Cmd/Ctrl + 单击` 终端输出中的文件路径与行列号直接跳转打开，悬停实时高亮。
- **批量粘贴与工具套件（Batch Paste / OTTY Suite）**：新增批量粘贴弹窗与多会话协同效率增强。

## 优化与修复
- **SSH 隧道、RDP 与终端核心增强**：优化 `wuji-data` / `wuji-windows` SSH 隧道与 RDP、Windows ConPTY 与 VT 解析稳定性，完善高危命令安全护栏、会话录制与手机扫码远程控制体验。
- **跨平台构建优化**：修复 Windows 交叉编译 C++/Objective-C 条件编译问题，优化 Linux Docker 容器发布构建内存占用。
