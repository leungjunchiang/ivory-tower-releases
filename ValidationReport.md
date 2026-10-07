# 象牙塔 0.4.1 验证记录

## 通过的验证

- GitHub Actions 原生构建 run [#37648037378](https://github.com/leungjunchiang/ivory-tower/actions/runs/37648037378) 中 Windows x64、macOS arm64 和 macOS Intel 三个任务均成功。
- 各平台站点测试 29 项通过；桌面打包测试 22 项通过，平台不适用的用例按 CI 标记跳过。
- 三个平台均完成原生窗口启动与首页/订阅流程烟测；Mac runner 额外完成 app、DMG 和 app.zip 构建。
- Windows 安装器为 92,634,112 bytes；macOS arm64 DMG 为 180,505,786 bytes；macOS Intel DMG 为 180,178,113 bytes，均低于各自体积目标。
- 更新清单中的三平台更新包大小与 SHA-256、发布目录校验清单、两份 Mac 原生构建 sidecar SHA-256 均与实际文件一致。
- 本机 29 项站点测试、界面组合筛选烟测、JavaScript/Python 静态检查及隐私检查已通过；图标与阅读器预览位于项目 outputs 目录。

## 发布限制说明

- Windows 安装包未使用代码签名证书；macOS 使用 ad-hoc 签名，未完成 Apple 公证。
- 三平台成功结果来自原生 GitHub Actions runners；本机 Windows 沙箱无法访问 WebView2 原生窗口，浏览器组件联网下载也受网络限制。
- 本次验证覆盖构建、打包、首启与更新相关测试，不包含对用户现有安装做破坏性替换。更新失败时保留旧版与个人资料的逻辑由桌面打包测试覆盖。

