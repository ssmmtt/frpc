## k2p荒野无灯版启用frp客户端：

由于无灯版自带FRP是Xfrp版本，配置后无法使用，后发现网上小伙伴已经有解决办法。

1、将配置好的frpc.ini上传到K2P目录“/etc/storag”

2、高级设置－自定义设置－脚本－在 WAN 上行/下行启动后执行:  中加上以下代码
```
sleep 10 && wget -P /tmp http://opt.cn2qq.com/opt-file/frpc && chmod 777 /tmp/frpc
/tmp/frpc -c /etc/storage/frpc.ini >/dev/null 2>&1 &
```
或
```
sleep 10 && wget -P /tmp https://raw.githubusercontent.com/pqguanyinli/frpc/master/frpc && chmod 777 /tmp/frpc
/tmp/frpc -c /etc/storage/frpc.ini >/dev/null 2>&1 &
```
3、重启路由

##
frpc frps.ini和frpc.ini 为本人自用，k2p路由器frpc最新客户端下载：http://opt.cn2qq.com/opt-file/

frp 官方使用详细说明：https://github.com/fatedier/frp/blob/master/README_zh.md

##
## vediotalk大神的frp安装方法 


