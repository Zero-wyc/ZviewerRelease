# ZViewer 预编译包

ZViewer 正式版的打包产物，由 GitHub Actions 自动发布，**每次发版整体替换**。

## 当前版本

| 项目 | 值 |
| --- | --- |
| 版本 | **v5.3.7** |
| 构建提交 | [`1466b1a`](https://github.com/Zero-wyc/ZViewer/commit/1466b1a65dfd2c2b0a147ef854364ca7edb9730b) |
| 发布时间 | 2026-11-28 16:45 UTC |

## 下载

| 平台 | 文件 | 大小 | 下载 |
| --- | --- | --- | --- |
| Windows 桌面版（推荐） | `zviewer-windows-x64-GUI.zip` | 61.5 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.3.7/zviewer-windows-x64-GUI.zip) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-windows-x64-GUI.zip?ref=main) |
| Windows 单文件 | `zviewer-windows-x64.zip` | 62.9 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.3.7/zviewer-windows-x64.zip) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-windows-x64.zip?ref=main) |
| Linux | `zviewer-linux-x64.tar.gz` | 61.6 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.3.7/zviewer-linux-x64.tar.gz) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-linux-x64.tar.gz?ref=main) |

桌面版解压后运行 `ZViewerDesktop.exe`，按界面提示启动服务；单文件版 Windows 运行 `start.bat`、Linux 运行 `./start.sh`。
启动后访问 `http://localhost:3333`，初始账号 `root` / `root`，登录后立即修改密码。

## 其他

- 更新日志：[GitHub Release v5.3.7](https://github.com/Zero-wyc/ZViewer/releases/tag/v5.3.7)
- 桌面端可选组件（cloudflared、EasyTier、frpc、livekit）：本仓库的 [`components` 分支](https://github.com/Zero-wyc/ZviewerRelease/tree/components)
- 校验：每个包的 SHA-256 见 `latest.json`
