## set-up-net-speeder

首次发表于[Shadowsocks(R)服务器部署](https://www.dominic-lian.space/?p=115)

### 安装NetSpeeder来加速代理速度
安装net-speeder安装上之后能提升代理速度, 但是流量X2

详细说明：[https://github.com/snooda/net-speeder](https://github.com/snooda/net-speeder)
#### 1.下载安装脚本
```
wget --no-check-certificate https://raw.githubusercontent.com/dominic-lian/set-up-net-speeder/master/set-up-net-speeder.sh
sh set-up-net-speeder.sh
```

#### 2.运行
```
nohup /usr/local/net_speeder/net_speeder venet0 "ip" >/dev/null 2>&1 &
```

#### 3.加入自启动
```
echo "nohup /usr/local/net_speeder/net_speeder venet0 "ip" >/dev/null 2>&1 &" >> /etc/rc.local
```
