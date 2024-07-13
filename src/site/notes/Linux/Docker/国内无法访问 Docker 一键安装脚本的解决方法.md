---
{"dg-publish":true,"dg-permalink":"note/21","permalink":"/note/21/","tags":["Linux","Docker"],"created":"2024-07-07 12:54:11","updated":"2024-07-07 13:35:22"}
---

Docker 的一键安装脚本的域名 `get.docker.com` 无法访问了怎么办？

```bash
root@debian:~# curl -fsSL https://get.docker.com | bash
curl: (35) Recv failure: Connection reset by peer
```

其实，这个脚本在 Github 上有个仓库，只要访问仓库里脚本的下载地址就好了。

```bash
curl -fsSL https://raw.githubusercontent.com/docker/docker-install/master/install.sh | bash
```

如果 Github 无法访问，还可以用 ghproxy。

```bash
curl -fsSL https://mirror.ghproxy.com/raw.githubusercontent.com/docker/docker-install/master/install.sh | bash
```