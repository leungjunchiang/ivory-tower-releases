# 象牙塔 · 公开发行

象牙塔是本机订阅、阅读与研究工作台。本仓库仅提供公开安装包、更新清单、校验值、使用说明与第三方许可；开发源码位于私有仓库。

## 下载象牙塔 0.4.0

打开[象牙塔 0.4.0 Release](https://github.com/leungjunchiang/ivory-tower-releases/releases/tag/v0.4.0)。GitHub 附件可匿名下载，无需登录。

- Windows x64：下载 `IvoryTower-Windows-x64-Setup.exe`，运行安装器，可选安装目录与快捷方式。
- Apple Silicon Mac：下载 `IvoryTower-macos-arm64.dmg`，将象牙塔拖入 Applications。
- Intel Mac：下载 `IvoryTower-macos-x64.dmg`，将象牙塔拖入 Applications。

请勿将 Mac `.app.zip` 当作首次安装包；它用于应用内一键更新。`SHA256SUMS.txt` 列出全部发行附件的 SHA-256，`update.json` 为应用更新器使用的版本清单。

## 本版功能

订阅中心按公众号、微博、小红书、期刊/RSS 和其它来源分类，支持粘贴链接识别来源。学术来源包含 Google Scholar、SSRN、NBER 和普通学术主页；同一研究者可合并多个主页。学术主页按重点/普通/静默低频检查；社交来源只读取匿名可见公开内容，不登录、不评论、不点赞、不转发或发帖。另支持公众号链接识别与应用内扫码授权、RSS/OPML、资料库、批注、Markdown/Obsidian 导出、搜索和完整包更新。

## 平台状态和访问范围

Windows 安装器未签名；macOS 使用 ad-hoc 签名，没有 Apple Developer 分发证书或 Apple 公证。Mac 主程序不捆绑 Chromium；需要浏览器的采集流程可使用现有兼容浏览器或按需安装独立组件。

Google Scholar 主页必须公开，才能匿名读取；其它学术主页、微博和小红书只按公开访客可见范围采集。公众号历史内容取决于用户本人在象牙塔内完成的授权通道及其可见范围。平台访问限制可能使资料不完整，软件不尝试绕过限制。

[使用说明](使用说明.md) · [验证记录](ValidationReport.md) · [第三方声明](THIRD_PARTY_NOTICES.md) · [许可](LICENSE)
