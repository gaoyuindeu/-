# -
在微信手机端和电脑端同时在同一网络下登陆时，会出现备份异常，即显示需要连接到同一网络。
![image](https://github.com/user-attachments/assets/c6e06108-3826-4fd4-996c-e1c059c7089a)

解决方案：建立虚拟WIFI网卡
1. 管理员下运行CMD
2. 运行命令：netsh wlan set hostednetwork mode=allow ssid=VituralAP key=123456789
3. 设置Internet共享：![image](https://github.com/user-attachments/assets/871ae57d-ce27-41c0-abf1-b37ce1a6a5d6)
4. 开启无线网络：CMD中输入netsh wlan start hostednetwork
5. 手机连接VituralAP这个wifi,密码为123456789
6. 开始通过微信传输文件。

如果想关闭虚拟网卡：
1. 运行CMD，输入：
netsh wlan stop hostednetwork
netsh wlan set hostednetwork mode=disallow
   
