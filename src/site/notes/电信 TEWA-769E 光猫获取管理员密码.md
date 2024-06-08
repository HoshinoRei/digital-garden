---
{"dg-publish":true,"dg-permalink":"note/6","permalink":"/note/6/","created":"2024-06-08 15:22:48","updated":"2024-06-08 15:42:09"}
---

## 教程

1. 准备一个 U 盘，格式化成 FAT32 格式，插入光猫的 USB 口
2. 打开 [http://192.168.1.1:8080](http://192.168.1.1:8080)，通过光猫背面的账号密码登录，默认用户名应该是 `useradmin`
3. 打开 [设备管理](http://192.168.1.1:8080/MD_Device_user.html)，在浏览器控制台的 Elements 中搜索 `set3_sessionKey` 并记下
4. 将 `sessionKey` 添加到 `http://192.168.1.1:8080/usbbackup.cmd?action=backupeble&set3_sessionKey=` 尾部并打开
5. 禁用 `快速恢复`，点击 `备份配置`
6. 拔下 U 盘并插入电脑，此时 U 盘根目录应该多了个 `e8_Config_Backup` 文件夹
7. 打开 [http://freevon.net/jm/](http://freevon.net/jm/)，配置文件选择 `e8_Config_Backup` 文件夹中的 `ctce8_TEWA-769E.cfg` 并转换
8. 搜索 `TeleComAccount`，如果附近有被 `<Password>` 包裹的字符串则该字符串就是光猫管理员密码

## 提示

光猫管理员账号一般是 `telecomadmin`
## 参考

1. [电信天翼网关TEWA-1000E/G等系列光猫破解超级密码](http://freevon.net/topic.asp?ID=31)