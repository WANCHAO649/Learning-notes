* 生产环境中的Node.js应用
* Windows + Linux
* VirtualBox

1. VirtualBox
2. 虚拟机CentOS安装
3. xShell与xFtp
3. Node.js
4. MongoDB
5. Redis
6. Sublime Text
7. WebStorm

WANCHAO888<br>
修改网卡配置：vi /etc/sysconfig/network-scripts/ifcfg-enp0s3<br>
G<br>
i<br>
ONBOOT=yes
键盘上的esc退出编辑<br>
:wq（保存）<br>
重启虚拟机网络：systemctl restart network<br>
ifconfig<br>
ping www.google.com

c:\Windows\System32\drivers\etc<br>
hosts<br>
192.168.??.??   geek

yum install epel-release<br>
yum install nodejs<br>
node --version<br>
yum install mongodb-server<br>
yum install mongodb<br>
mongo --version<br>
yum install redis<br>
redis-cli --version<br>
