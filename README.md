# 象牙塔 · 公开发行

象牙塔是本机订阅、阅读与研究工作台。本仓库提供公开安装包、更新清单、校验值、使用说明与第三方许可；开发源码仓库保持私有。

## 下载象牙塔 0.4.1

打开[象牙塔 0.4.1 Release](https://github.com/leungjunchiang/ivory-tower-releases/releases/tag/v0.4.1)。附件可匿名下载，无需登录。

- Windows x64：[下载安装器](https://github.com/leungjunchiang/ivory-tower-releases/releases/download/v0.4.1/IvoryTower-Windows-x64-Setup.exe)
- Apple Silicon Mac：[下载 DMG](https://github.com/leungjunchiang/ivory-tower-releases/releases/download/v0.4.1/IvoryTower-macos-arm64.dmg)
- Intel Mac：[下载 DMG](https://github.com/leungjunchiang/ivory-tower-releases/releases/download/v0.4.1/IvoryTower-macos-x64.dmg)

Mac `.app.zip` 文件用于应用内一键更新，首次安装请使用 DMG。Release 附有 `SHA256SUMS.txt` 校验清单与 `update.json` 更新元数据。首次安装前请核对校验值。

## 0.4.1 更新

- 今日、资料库、订阅统一来源分类顺序；今日和资料库支持组合来源类型与阅读状态筛选。
- 重点、普通、静默采用三段式关注控制；`priority` 是唯一可编辑状态，并显示保存结果。
- 公众号订阅与补历史解耦：粘贴推文链接即可订阅，授权与历史扫描可按需进行。
- 学术主页和 SSRN 遇到匿名访问限制时保留订阅并低频重试；期刊 RSS 与其它 RSS 分开归类。

## 本版功能

订阅中心支持公众号、微博、小红书、学术主页、期刊/RSS 和其它来源。可粘贴链接识别来源，也支持 RSS/Atom 与 OPML。学术主页包含 Google Scholar、SSRN、NBER 和普通学术主页；同一研究者可合并多个主页。微博和小红书只读取匿名访客可见的公开内容，不登录，不提供评论、点赞、转发或发帖。资料库支持阅读状态筛选、批注、Markdown/Obsidian 导出和搜索。

## 平台状态和访问范围

Windows 安装器未签名；macOS 使用 ad-hoc 签名，没有 Apple Developer 分发证书或 Apple 公证。Mac 主程序不捆绑 Chromium；需要浏览器的采集流程可使用本机兼容浏览器或按需安装独立组件。

Google Scholar 主页必须公开后才能匿名读取；微博、小红书和其它学术主页只按公开访客可见范围采集。公众号历史内容取决于用户本人在象牙塔内完成的授权通道及其可见范围。平台访问限制可能使资料不完整，软件不尝试绕过限制。

[使用说明](使用说明.md) · [验证记录](ValidationReport.md) · [第三方声明](THIRD_PARTY_NOTICES.md) · [许可](LICENSE)
