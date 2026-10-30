# ZViewer 预编译包

ZViewer 正式版的打包产物，由 GitHub Actions 自动发布，**每次发版整体替换**——仓库里只有当前版本。
源码、文档与问题反馈在 [Zero-wyc/ZViewer](https://github.com/Zero-wyc/ZViewer)。

## 当前版本

| 项目 | 值 |
| --- | --- |
| 版本 | **v5.1.5** |
| 构建提交 | [`ea953c2`](https://github.com/Zero-wyc/ZViewer/commit/ea953c21f6db1bafafaa4ccdc06977b54f5fb506) |
| 发布时间 | 2026-10-30 16:32 UTC |

## 下载

| 平台 | 文件 | 大小 | 下载 |
| --- | --- | --- | --- |
| Windows 桌面版（推荐） | `zviewer-windows-x64-GUI.zip` | 28.5 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.1.5/zviewer-windows-x64-GUI.zip) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-windows-x64-GUI.zip?ref=main) |
| Windows 单文件 | `zviewer-windows-x64.zip` | 19.8 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.1.5/zviewer-windows-x64.zip) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-windows-x64.zip?ref=main) |
| Linux | `zviewer-linux-x64.tar.gz` | 37.0 MB | [GitHub](https://github.com/Zero-wyc/ZViewer/releases/download/v5.1.5/zviewer-linux-x64.tar.gz) · [GitCode](https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/zviewer-linux-x64.tar.gz?ref=main) |

桌面版解压后运行 `ZViewerDesktop.exe`，按界面提示启动服务；单文件版 Windows 运行 `start.bat`、Linux 运行 `./start.sh`。
启动后访问 `http://localhost:3333`，初始账号 `root` / `root`，登录后立即修改密码。

## latest.json

更新器读的版本清单：`tag` / `version` / `commit` / `publishedAt`，每个包带 `size` / `sha256` / `url`。

```text
https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/latest.json?ref=main
```

客户端按它判断有没有新版本，境内直连、不需要代理。

## 其他

- 更新日志：[GitHub Release v5.1.5](https://github.com/Zero-wyc/ZViewer/releases/tag/v5.1.5)
- 桌面端可选组件（cloudflared、EasyTier、frpc、livekit）：本仓库的 [`components` 分支](https://github.com/Zero-wyc/ZviewerRelease/tree/components)，不随发版替换
- 校验：每个包的 SHA-256 见 `latest.json`
