---
{"dg-publish":true,"dg-permalink":"note/18","permalink":"/note/18/","tags":["Linux","Openwrt","ImmortalWrt"],"created":"2024-06-30 10:43:09","updated":"2024-06-30 11:24:04"}
---

## 教程

首先替换下载地址。由于 ImmortalWrt 的默认 shell 是 ash，粘贴命令可能不完整，可以通过先执行 `bash` 命令切换到 bash。如果要修改默认 shell 为 bash，请看《[[Linux/Openwrt/ImmortalWrt 更改默认 shell 为 bash\|ImmortalWrt 更改默认 shell 为 bash]]》。

```bash
sed -e 's,downloads.immortalwrt.org,mirrors.cernet.edu.cn/immortalwrt,g' -e 's,mirrors.vsean.net/openwrt,mirrors.cernet.edu.cn/immortalwrt,g' -i.bak /etc/opkg/distfeeds.conf
```

更新源。

```bash
opkg update
```

## 参考

1.[ImmortalWrt 软件仓库镜像使用帮助](https://help.mirrors.cernet.edu.cn/immortalwrt/)