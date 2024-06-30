---
{"dg-publish":true,"dg-permalink":"note/19","permalink":"/note/19/","tags":["Linux","Openwrt","ImmortalWrt"],"created":"2024-06-30 11:12:40","updated":"2024-06-30 11:17:30"}
---

## 教程

ImmortalWrt 的默认 shell 是 ash，现在要更改为 bash。

执行以下命令：

```ash
sed -e 's,root:x:0:0:root:/root:/bin/ash,root:x:0:0:root:/root:/bin/bash,g' -i /etc/passwd
```

## 参考

1.[更换openwrt shell解析器为bash,解决history不保存问题](https://www.openwrt.pro/post-598.html)