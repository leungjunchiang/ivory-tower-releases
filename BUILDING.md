# 从私有源码构建桌面发行版

公开发布仓库中的 Actions 工作流会在 GitHub 标准公开 runner 上构建 Windows、macOS Apple Silicon 和 macOS Intel 安装包。源码仍保存在私有仓库 `leungjunchiang/ivory-tower`，工作流只检出你指定的源码标签，并把最终附件发布到本仓库。

## 一次性设置私有源码只读令牌

1. 在 [Fine-grained personal access tokens](https://github.com/settings/personal-access-tokens/new) 创建令牌。
2. Repository access 选择 **Only select repositories**，只选 `ivory-tower`。
3. Repository permissions 只授予 **Contents: Read-only**。不需要写权限、Actions 权限或组织权限。
4. 到 [本仓库 Actions secrets 设置](https://github.com/leungjunchiang/ivory-tower-releases/settings/secrets/actions/new)，名称填 `SOURCE_REPO_READ_TOKEN)，值粘贴刚创建的令牌。令牌不要提交到仓库或发到聊天。

## 构建和发布

打开 [Build and publish IvoryTower desktop release](https://github.com/leungjunchiang/ivory-tower-releases/actions/workflows/build-desktop-from-private.yml)，点击 **Run workflow**，输入已经推送到私有源码仓库的标签，例如 `v0.4.28`。

工作流会先运行 Windows 和两个 macOS 构建及测试；三个平台均成功后，才会创建或更新本仓库的 Release，并上传安装包、应用更新包、`update.json` 与 SHA-256 校验清单。失败时不会发布不完整的版本。

工作流只响应手动触发，不会因公开仓库中的 Pull Request 运行，也不会在构建步骤保留私有仓库访问令牌。
