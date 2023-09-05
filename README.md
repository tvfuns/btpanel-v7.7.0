
### 一键安装7.7版本

适用 Centos/Ubuntu/Debian

```
curl -sSO https://raw.githubusercontent.com/woniu336/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```

`安装完成后,解除进入面板需要账号密码:`

```bash
rm -f /www/server/panel/data/bind.pl
```

`执行以下内容，避免官方搞小动作`

```bash
echo '127.0.0.1 bt.cn' >>/etc/hosts
```



### **手动解锁宝塔所有付费插件为永不过期**

文件路径：`/www/server/panel/data/plugin.json`

搜索字符串：`"endtime": -1` 全部替换为 `"endtime": 999999999999`



###   给plugin.json文件上锁防止自动修复为免费版

```shell
chattr +i /www/server/panel/data/plugin.json
```



注意事项 : 服务器重启后又回到"endtime": -1 需要再次修改替换

### 净化面板


下载文件
```
wget -O /tmp/bt.zip https://github.com/woniu336/btpanel-v7.7.0/raw/main/bt/bt.zip
```
解压文件并合并到目标目录 (选A 同意覆盖所有)
```
unzip -u /tmp/bt.zip -d /www/server/panel/BTPanel/templates/default
```

删除下载的压缩文件（如果需要）

```
rm /tmp/bt.zip
```

### 最后重启面板生效

完结撒花🤡

fuck bt 🤡🤡🤡

<p>