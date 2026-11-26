# WujiTerm v0.6.11

## 新特性与优化
- 后台更新检查优化为应用启动 3 分钟后首次静默检查，之后每隔 4 小时检查一次，无轮询开销，避免启动阶段资源竞争。
- 更新检查策略新增「不检查更新」选项，选择后不执行后台定时检查，仅支持手动触发检查。

## 跨平台安装包与校验 (SHA-256)
- `WujiTerm-0.6.11-macos-universal.dmg`: `496b4b82961c84d00557ce69cafbd072e54242a6c9455a2b1375135e21db1389`
- `WujiTerm-linux-x86_64.tar.gz`: `f324693b9df3ef9e14f838c081efddb7d29c4677fceb7310c12c3e3fab5477f0`
- `WujiTerm-cli-tools-linux-x86_64.tar.gz`: `14e9961e6271d967142ecea283335067c745d4e01b5a1cbe58ce62b8379ae20d`
- `WujiTerm-linux-aarch64.tar.gz`: `e525dd11e2b77bb162f5fe30e7fb6daf63c31ec7963d0094d45ee661813e7869`
- `WujiTerm-cli-tools-linux-aarch64.tar.gz`: `e6a1e9e25c7a71b4d38e256d0c545899092c5299a93145eebda5350803001d26`
- `WujiTerm-windows-x86_64.zip`: `d3f735fa8b54bf721e5b9b41c2712eb251d4d9bb802c8035e01bd9fe2fcaaa47`
- `WujiTerm-cli-tools-windows-x86_64.zip`: `71ecea793eae360329c048b86dff1abfdc5ed0c38c55cd6c30d30e545074ecab`
