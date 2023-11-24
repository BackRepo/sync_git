# 避难所 Shelter

## 项目描述 Project Description

这个项目是一个用于同步GitHub仓库到GitLab的工具。它可以帮助你备份你的代码，防止因各种原因导致的仓库被屏蔽、下架、删除或违规。

This project is a tool for synchronizing GitHub repositories to GitLab. It can help you back up your code to prevent your repositories from being blocked, removed, deleted, or violated for various reasons.

## 使用方法 Usage

1. 克隆本仓库到你的本地机器。

- Clone this repository to your local machine.

2. 在`.github/workflows/sync.yml`文件中，找到`jobs` -> `sync` -> `strategy` -> `matrix` -> `REPO_URL`，并将其值设置为你想要同步的GitHub仓库的URL。

- In the `.github/workflows/sync.yml` file, find `jobs` -> `sync` -> `strategy` -> `matrix` -> `REPO_URL` and set its value to the URL of the GitHub repository you want to synchronize.

3. 提交并推送你的更改。

- Commit and push your changes.

以下是具体的命令：

Here are the specific commands:

```bash
# 克隆本仓库 / Clone this repository
git clone https://github.com/1299172402/sync_git.git

# 进入仓库目录 / Enter the repository directory
cd sync_git

# 编辑同步配置文件 / Edit the sync configuration file
nano .github/workflows/sync.yml

# 提交并推送你的更改 / Commit and push your changes
git add .github/workflows/sync.yml
git commit -m "Update sync configuration"
git push
```

## 配置示例 Configuration Example

在`.github/workflows/sync.yml`文件中，你可以设置多个仓库进行同步，如下所示：

In the `.github/workflows/sync.yml` file, you can set multiple repositories to synchronize, as shown below:

```yaml
jobs:
  sync:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        REPO_URL:
          - 'https://github.com/2dust/v2rayN.git'
          - 'https://github.com/2dust/v2rayNG.git'
```

你可以在[这里](.github/workflows/sync.yml)查看已经配置的同步仓库列表。

You can view the list of configured sync repositories [here](.github/workflows/sync.yml).

所有同步的仓库都会被推送到我们的[GitLab项目](https://gitlab.com/mirrors_git)。

All synchronized repositories will be pushed to our [GitLab project](https://gitlab.com/mirrors_git).

## 贡献 Contribution

如果你有任何想法或者建议，欢迎提交 issue 或者 pull request。

If you have any ideas or suggestions, feel free to submit an issue or pull request.
