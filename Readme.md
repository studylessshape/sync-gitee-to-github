# Gitee 仓库同步到 Github（支持私有仓库）
- [使用 ssh](ssh-to-gitee.yml)
- [使用 Gitee Open API](gitee-open-api.yml)

## 公开仓库更加方便的同步 Action
- [hub-mirror-action](https://github.com/Yikun/hub-mirror-action)

## 使用 ssh 的 Github action 说明
将文件中的环境变量配置好，并为 Github 仓库配置好 `Secrets and Variables` -> `Action` 中的仓库秘密，需要的字段说明如下：
- `GITEE_SSH_PRIVATE_KEY`：ssh 连接的私钥
- `REPO_TOKEN`：Github 有仓库权限的 Token

**注意**：一定不要泄露私钥和 Token。

最后的 `git push github master -f` 为强制推送，可以删除 `-f` 设置来取消强制推送。

## 使用 Gitee Open API 说明
将文件中尖括号全替换为自己的内容。

在 Gitee 的个人设置中生成一个私人令牌，并在 Github 仓库的 `Secrets and Variables` -> `Action` 配置，需要的字段说明如下：
- `GITEE_ACCESS_TOKEN`：Gitee 的私人令牌
