# ZViewer 预编译包

ZViewer 正式版的打包产物，由 GitHub Actions 自动发布，**每次发版整体替换**。

## 当前版本

| 项目 | 值 |
| --- | --- |
| 版本 | **v5.2.2** |
| 构建提交 | [`dcf223f`](https://github.com/Zero-wyc/ZViewer/commit/dcf223f5405217956c3f323d59ca54c825b389e6) |
| 发布时间 | 2026-11-07 11:56 UTC |

## 下载

| 平台 | 文件 | 大小 | 下载 |
| --- | --- | --- | --- |
| Windows 桌面版（推荐） | `zviewer-windows-x64-GUI.zip` | 36.2 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.2.2/zviewer-windows-x64-GUI.zip) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-windows-x64-GUI.zip?ref=main) |
| Windows 单文件 | `zviewer-windows-x64.zip` | 27.7 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.2.2/zviewer-windows-x64.zip) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-windows-x64.zip?ref=main) |
| Linux | `zviewer-linux-x64.tar.gz` | 27.2 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.2.2/zviewer-linux-x64.tar.gz) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-linux-x64.tar.gz?ref=main) |

桌面版解压后运行 `ZViewerDesktop.exe`，按界面提示启动服务；单文件版 Windows 运行 `start.bat`、Linux 运行 `./start.sh`。
启动后访问 `http://localhost:3333`，初始账号 `root` / `root`，登录后立即修改密码。

## 其他

- 更新日志：[GitHub Release v5.2.2](https://github.com/Zero-wyc/ZViewer/releases/tag/v5.2.2)
- 桌面端可选组件（cloudflared、EasyTier、frpc、livekit）：本仓库的 [`components` 分支](https://github.com/Zero-wyc/ZviewerRelease/tree/components)
- 校验：每个包的 SHA-256 见 `latest.json`
