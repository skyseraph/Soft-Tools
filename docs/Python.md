# Python

- [Anaconda](https://www.continuum.io/) Python 多版本管理工具
- [virtualenv](https://virtualenv.pypa.io/en/stable/) 虚拟环境虚拟环境
- [pyenv](https://github.com/pyenv/pyenv) 虚拟环境虚拟环境

## 实用命令

- 解压zip压缩包： python -m zipfile -l xx.zip

- 检查三方库是否安装成功：  python -c "import xx"

## Anaconda 专题

> 基础 

- conda config --show  	# 查看配置信息    
- conda --version			# 查看版本号    
- conda update conda		# 升级当前版本的conda  
- conda update anaconda	# 更新anaconda  
- conda update python		# 更新python至当前系列最新版  

> 环境管理(python)

1. 创建一个2.7.×的python环境  
conda create --name python27 python=2.7  
2. 创建一个3.4.×的python环境  
conda create --name python34 python=3.4   
3. 查看现在所在的版本分支  
conda info --e  
4. 切换到你所需要的分支  
source activate bunnies # for Linux & Mac  
activate bunnies # for Windows  
5. 返回默认的python环境  
deactivate python34 # for Windows  
source deactivate python34 # for Linux & Mac  
6. 删除一个已有的环境  
conda remove --name python34 --all  

> 包管理

- conda list 				# 查看当前环境下已安装包列表  
- conda list -n python34	# 查看某个指定环境的已安装包  
- conda search numpy		# 查找package信息  
- conda install numpy		# 当前环境安装package  
- conda install -n python34 numpy	# 指定环境安装package  
- conda update -n python34 numpy	# 更新package  
- conda remove -n python34 numpy	# 删除package  
- conda install anaconda	# 在当前环境下安装anaconda包集合  
- 
> 设置国内镜像

- conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/ # 添加Anaconda的TUNA镜像
- conda config --set show_channel_urls yes # 设置搜索时显示通道地址

> 代理设置

- 路径： C:\Users\name\.condarc 文件  # for windows
- proxy_servers:  
    http: http://user:pass@corp.com:8080  
    https: https://user:pass@corp.com:8080

> 实用参考

- [Anaconda Homepage](https://www.continuum.io/why-anaconda)
- [Anaconda Documentation](https://docs.continuum.io/anaconda/index)
- [Conda Docs](http://conda.pydata.org/docs/index.html)
