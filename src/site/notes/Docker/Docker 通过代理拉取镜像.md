---
{"dg-publish":true,"dg-permalink":"note/2","permalink":"/note/2/","tags":["Docker"],"created":"2024-06-07 21:48:31","updated":"2024-06-30 10:51:52"}
---

编辑 `/etc/docker/daemon.json`

```bash
sudo vim /etc/docker/daemon.json
```

写入

```json
{
 "proxies": {
   "default": {
     "httpProxy": "http://:",
     "httpsProxy": "http://",
     "noProxy": ""
   }
 }
}
```

示例

```json
{
 "proxies": {
   "default": {
     "httpProxy": "http://proxy.example.com:3128",
     "httpsProxy": "https://proxy.example.com:3129",
     "noProxy": "*.test.example.com,.example.org,127.0.0.0/8"
   }
 }
}
```

## 参考
1. [Configure the Docker client](https://docs.docker.com/network/proxy/#configure-the-docker-client)