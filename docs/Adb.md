# Adb
Adb commands

## 辅助工具

- [Packet Sender](https://github.com/dannagle/PacketSender)  Android ADB 端口转发调试工具


## 常用adb命令 

- adb **kill-server**

- adb **devices**  

- adb **install** [-l] [-r] [-s] <file>        
    -l 表示锁定该程序;   
    -r 表示替换原有的apk安装;   
    -s 表示安装在SD卡内，而不是设备内部存储

- adb **uninstall** [-k] <package>             
    -k 表示不删除程序运行所产生的数据和缓存目录(如软件的数据库文件)

- adb shell pm clear  <package>    
清除应用缓存

- taskkill /f /im adb*  

- adb shell getprop ro.build.version.release  版本

- adb shell + cat /system/build.prop  查看手机配置信息

- adb shell getprop dalvik.vm.heapsize  

> **获取进程号**    

- adb shell  
- ps | grep 进程名  
- cat /proc/pid/oom_adj  //其中**pid**是上述grep得到的进程号     


> **查看包名相关**    

- adb shell pm list package [-f]  获取手机内所有包名    
    -f 包名+路径    

- **adb shell dumpsys window w | findstr \/ | findstr name=**    
查看包名   

- adb shell dumpsys activity> d:\log.txt   
导出包名（log中搜索 Stack #1，然后寻找cmp=）   

- adb shell + logcat | grep START   


## 实用参考  






