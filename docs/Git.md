# Git
Git commands


## 常用Git命令

> 汇总   

- git log  历史记录

- git status  

- git clean -df	  

- git branch -vv  


> **Git配置相关**    

- git config -l   
查看Git当前配置信息

- 配置  
git config --global user.email "you@email.com"    
git config --global user.name "Your Name"    
git config --global core.editor "nano"     
git config --global color.ui true    

> **删除远程分支A**    

- git push origin --delete A    

- git push origin :A    


> **回退**    

- 远程服务器支持SSH前提下    

git reset –mixed   // 此为默认方式，不带任何参数的git reset，就是这种方式，它回退到某个版本，只保留源码，回退commit和stage信息

git reset –soft    // 回退到某个版本，只回退了commit的信息，不会恢复stage（如果还要提交，直接commit即可)

git reset –hard    // 彻底回退到某个版本， 本地的源码也会变为上一个版本的内容

- 远程服务器不支持SSH    

git branch old_master  //新建old_master分支 作为备份，以防万一

git push origin old_master:old_master //将本地的old_master分支　推送到远程的old_master

git reset –hard //本地仓库　彻底回退到某一个版本

git push origin :master // 删除远程的master分支

git push origin master //重新创建远程master分支


## 实用参考  

- [《Git权威指南》]()

- [《Git Community Book 中文版》](http://gitbook.liuhui998.com/index.html)

- [Git的奇技淫巧](https://github.com/521xueweihan/git-tips)





