# finalspeed

##  开放端口
```bash
service iptables start
iptables -A INPUT -p tcp --dport 你的vps端口号 -j ACCEPT
iptables -A OUTPUT -p tcp --sport 你的vps端口号 -j ACCEPT
service iptables save
```

## 安装命令:

```bash
rm -f install_fs.sh
wget  https://github.com/ucoker/finalspeed/raw/master/install_fs.sh
chmod +x install_fs.sh
./install_fs.sh 2>&1 | tee install.log
```

## 其他使用说明

* 更新：执行一键安装会自动完成更新。
* 卸载：  
`sh /fs/stop.sh ; rm -rf /fs`
* 启动：  
`sh /fs/start.sh`
* 停止：  
`sh /fs/stop.sh`
* 重新启动：  
`sh /fs/restart.sh`
* 运行日志：  
`tail -f /fs/server.log`


## 参考
* https://github.com/dupontjoy/customization/tree/master/Rules/Shadowsocks/Finalspeed

