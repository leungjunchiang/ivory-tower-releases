# 象牙塔 0.4.0 验证记录

记录日期：2026-10-07。源码版本和发行附件均依据私有仓库 `leungjunchiang/ivory-tower` 的 `v0.4.0` 标签构建。

## 源码与构建

- 默认分支 `main` 版本文件为 `0.4.0`。
- 源码提交：`415a202ae5a17a96c64df887c16eaeafd654569f`；Git tree：`b0a54ea6751b6713120d9338568d13fcd3791606`。
- 标签：`v0.4.0`，指向上述 main 提交。
- 原生 CI：[GitHub Actions run 37624569668](https://github.com/leungjunchiang/ivory-tower/actions/runs/37624569668)，Windows x64、macOS arm64 和 Intel 三个 job 均通过。
- 开发源码仓库保持私有；公开发行仓库为 `leungjunchiang/ivory-tower-releases`。

## 包体积

MB 按 1,000,000 字节计算，SHA-256 见随附 `SHA256SUMS.txt`。Windows 安装器目标小于 180 MB，两种 Mac DMG 目标小于 350 MB。

| 文件 | 字节 | MB |
| --- | ---: | ---: |
| `IvoryTower-Windows-x64-Setup.exe` | 92,629,504 | 92.63 |
| `IvoryTower-macos-arm64.dmg` | 182,205,779 | 182.21 |
| `IvoryTower-macos-arm64.app.zip` | 134,107,712 | 134.11 |
| `IvoryTower-macos-x64.dmg` | 180,527,093 | 180.53 |
| `IvoryTower-macos-x64.app.zip` | 132,284,992 | 132.28 |

## 自动化验证

- `site/tests`：23 项通过，覆盖 RSS、微博/小红书公开解析、学术主页 URL 识别与解析、NBER/SSRN/Scholar 低频节奏、研究者实体合并、状态持久化与搜索。
- `packaging/tests`：Windows 本机 16 项通过、6 项 Mac 原生用例按平台跳过；macOS arm64 和 Intel runner 均通过对应的平台测试。
- 原生桌面窗口：三个原生 runner 验证免密码首次进入、四项一级导航、六类订阅筛选、统一链接识别表单、公众号高级选项与应用功能冒烟。
- Windows 安装器：基于实际 `Installer.cs` 的隔离测试覆盖自定义登记目录、静默更新从注册表的 `InstallLocation` 原位替换、旧进程等待、失败时保留旧版和个人数据。首次安装界面提供路径、桌面/开始菜单快捷方式和完成后启动选项。
- Playwright 页面验证通过：订阅分类、公众号/微博/小红书链接路由与表单回填、研究者多主页合并资料流和关联新学术主页；无 JavaScript 页面异常。界面预览见上层输出 `../象牙塔-0.4.0-订阅.png`。
- Windows、Apple Silicon 与 Intel Mac 标签构建、原生窗口冒烟和按需浏览器组件测试均通过。

## 访问限制与未覆盖情形

- Google Scholar 主页必须公开后才可匿名读取；[Google Scholar 官方说明](https://scholar.google.com/intl/en/scholar/citations.html)说明私有资料仅对所有者可见。
- NBER、SSRN 与普通学术主页只读取匿名可访问的论文链接。页面结构变化、反爬限制或 JS-only 内容可能减少条目；不会尝试登录或绕过验证。
- 微博和小红书仅覆盖匿名可见内容，不保证完整历史；不提供评论、点赞、转发或发帖。
- 公众号推文链接识别与二维码生成已有此前验证记录；本次没有取得用户扫码授权回执，扫码后历史采集、续扫和覆盖范围尚未验证。
- Windows 安装器未签名；macOS 使用 ad-hoc 签名，没有 Apple Developer 分发证书，也未完成 Apple 公证。


## 公开下载核验

- 未登录访问核验时间：`2026-10-07T13:22:26Z`。Release 页面返回 HTTP 200。
- 以下发行附件均通过匿名 GET 完整读取，并与本地文件字节数及 SHA-256 一致：

| 文件 | HTTP | 字节 | SHA-256 |
| --- | ---: | ---: | --- |
| `IvoryTower-macos-arm64.app.zip` | 200 | 134,107,712 | `965af3e31dbe65eb21d6053d5b3b1889d5bf9974ec40638d3642389d367dbad3` |
| `IvoryTower-macos-arm64.dmg` | 200 | 182,205,779 | `e0eaa19ba6cb8d258dc11f1e1977f436acca969c3b1a21654ed9a9f73b4fc370` |
| `IvoryTower-macos-x64.app.zip` | 200 | 132,284,992 | `775b58ef098f809f73b1c489aadc032a35b00fb2904e45c4e4af83813aab4822` |
| `IvoryTower-macos-x64.dmg` | 200 | 180,527,093 | `e7ec71f9ded0ec66c26c7f97c7d7ee6925819020d1b56b84a8098d6de89859bf` |
| `IvoryTower-Windows-x64-Setup.exe` | 200 | 92,629,504 | `cb6a370f4da5bc18108e6060f2a368cf34200a3755fc45ac5ca319940d1cfaab` |
| `LICENSE` | 200 | 1,090 | `6a6152a768403cc352ee2a1399b9ec1aff57fad837883717d23b2cdcdbe4ae97` |
| `THIRD_PARTY_NOTICES.md` | 200 | 1,606 | `a0bcf9d8853549dc7df8e853afd9fbb0b51e152c5cb422a275a8cb2d89e6f970` |
| `update.json` | 200 | 1,356 | `1b29fe8463ef14722e87671289fa2496c93dd303486aa77fa9b1522538b12221` |
| `UserGuide.md` | 200 | 4,402 | `5ce475060296c1634eb0054300733f366b336847a71d19f4371198ee1e553d11` |
| `ValidationReport.md` | 200 | 3,555 | `db461b02208961a4b1befa2af97670c2e41015736c6ec9e0f64c1a3fbe9f97ad` |
