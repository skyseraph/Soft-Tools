# Adb
Adb commands

## 辅助工具

- [Packet Sender](https://github.com/dannagle/PacketSender)  Android ADB 端口转发调试工具

- [ADBWIFI](https://github.com/layerlre/ADBWIFI) Android Studio plugin for debug android app over Wi-Fi

## 常用adb命令 

- adb version

- adb devices adb版本

- adb get-serialno 设备的序列号

- adb get-state 设备状态

- adb **kill-server**

- adb start-server

- adb **devices**  

- adb **install** [-l] [-r] [-s] file        
    -l 表示锁定该程序;   
    -r 表示替换原有的apk安装;   
    -s 表示安装在SD卡内，而不是设备内部存储

- adb **uninstall** [-k] package             
    -k 表示不删除程序运行所产生的数据和缓存目录(如软件的数据库文件)

- adb pull remote local

- adb push local remote

- adb forward local remote 端口映射  
adb forward tcp:5555 tcp:9001 // 把PC端5555端口的数据, 转发到Android端的9001端口上.

- adb shell pm clear  package    
清除应用缓存

- taskkill /f /im adb*  

- adb shell getprop ro.build.version.release  版本

- adb shell + cat /system/build.prop  查看手机配置信息

- adb shell getprop dalvik.vm.heapsize  

> [**dumpsys**](https://source.android.com/devices/input/diagnostics.html)  

- dumpsys [options]  
         meminfo 显示内存信息  
         cpuinfo 显示CPU信息  
         account 显示accounts信息  
         activity 显示所有的activities的信息  
         window 显示键盘，窗口和它们的关系  
         wifi 显示wifi信息  
         and so on  

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

- [ADB 用法大全](https://github.com/mzlogin/awesome-adb)




