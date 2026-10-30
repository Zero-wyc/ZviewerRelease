# ZviewerRelease · 组件库分支

这里是 ZViewer 桌面端的**可选组件库**（原 `Zero-wyc/ZViewer` 仓库的 `public/` 目录，2026-10-30 迁到本分支）。
不是网页静态资源，也不参与发版产物。

| 文件 | 版本 | 用途 |
| --- | --- | --- |
| `cloudflared-windows-amd64.exe` | 2026.10.3 | Cloudflare Tunnel（「一键启动隧道」） |
| `easytier-windows-x86_64-v2.6.4.zip` | 2.6.4 | EasyTier 虚拟组网（官方原包，安装时只解出 core/cli 与两个驱动） |
| `frp_0.71.1_windows_amd64.zip` | 0.71.1 | FRP 客户端（官方原包，安装时只解出 `frpc.exe`；服务端 `frps` 由用户自己在 VPS 上跑） |
| `livekit_1.13.7_windows_amd64.zip` | 1.13.7 | 语音聊天用的 LiveKit SFU（官方原包，安装时只解出 `livekit-server.exe`） |
| `LICENSE-EasyTier.txt` | — | EasyTier 是 LGPL-3.0，随二进制一起分发 |
| `components.json` | — | 上面几个文件的版本、大小与 SHA-256，供发版自检与人工核对 |

FRP 与 LiveKit 的 Apache-2.0 许可证就在各自官方 zip 内的 `LICENSE`，不必单独放一份。

## 谁来下载

| 组件 | 触发方 |
| --- | --- |
| cloudflared / EasyTier / frpc | 桌面 GUI 的「一键隧道 / 组网 / FRP 穿透」页，点下载后由壳安装到运行包 |
| livekit | **后端**（`backend-go/internal/livekit`）：房间右下角「语音聊天」面板缺组件时点下载，装到 `runtime/livekit-server.exe`，装完立即拉起，不用重启 |

后端下载也走本分支，顺序是 GitCode raw → GitHub raw → 官方 Release，前一个失败自动换下一个。

## 为什么在 `components` 分支，而不是 `main`

`main` 是发版产物分支：每次正式发版都会用**孤儿提交整体替换**（只留当前版本的三个安装包 + `latest.json`），
历史不累积。组件库需要跨版本长期存在，放 `main` 会被下次发版清掉，所以单独一条分支。

## 下载地址

桌面端用的是 **api/v5 的 raw 端点**（按字节返回，`application/octet-stream`，支持 Range）：

```
https://api.gitcode.com/api/v5/repos/Zero-wyc/ZviewerRelease/raw/<文件名>?ref=components
```

**不要**换成 `https://raw.gitcode.com/...`：那是站点「预览」通道，除被预览过的文档外
一律 `403 暂不支持预览`，exe/zip 永远下不到。

## 升级组件

1. 在 `Zero-wyc/ZViewer` 仓库跑 `desktop/scripts/fetch-components.ps1` 下载新版本到临时目录
   （或直接取上游官方发布）。
2. 更新本分支的文件，同时改 `components.json` 里的 `version` / `size` / `sha256`。
3. 同步客户端的版本与文件名：
   - cloudflared / EasyTier / frpc：`desktop/controller/components.go`（FRP 的版本同时是
     `controller.FrpVersion`，连接前的 `frpc --version` 会校验，两处必须一起改）；
   - LiveKit：`backend-go/internal/livekit/livekit.go` 的 `BinaryVersion`，以及 `build-all.js`
     里的 `LIVEKIT_VERSION`（Linux 产物仍随包带二进制）。
4. 提交推送本分支，等 GitCode 镜像追上后直链即刻生效。
