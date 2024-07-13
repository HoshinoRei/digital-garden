---
{"dg-publish":true,"dg-permalink":"note/22","permalink":"/note/22/","tags":["Windows","Scoop","NodeJS","nvm"],"created":"2024-07-13 16:16:03","updated":"2024-07-13 16:20:12"}
---

通过 Scoop 安装。

```powershell
scoop install main/nvm
```

设置 Node.js 安装包的镜像，这里实测阿里云、华为云的镜像是无法使用的。都提示缺少文件，中科大的是可以正常使用的。

```powershell
nvm node_mirror https://mirrors.ustc.edu.cn/node
```