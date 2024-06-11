# Install scRNAtoolVis by linux
# 安装scRNAtoolVis时遇到的错误

---  
### 1.安装scRNAtoolVis  
    devtools::install_github('junjunlab/scRNAtoolVis')  
### 2.安装scRNAtoolVis时没有magick这个包（服务器没有这个库文件）  
![0.png](https://github.com/y741269430/Install-scRNAtoolVis/blob/main/png/0.png)  
### 3.然后去服务器安装库  
#### linux 中运行(https://docs.ropensci.org/magick/articles/intro.html)    
    sudo apt-get install libmagick++-dev  
#### R 中运行  
    install.packages('magick')  
![1.png](https://github.com/y741269430/Install-scRNAtoolVis/blob/main/png/1.png)  

---  
### 4.安装ggunchull
    devtools::install_github("sajuukLyu/ggunchull", type = "source")
### 5.安装ggunchull时没有splancs这个包（服务器没有没有找到gfortran）  
![2.png](https://github.com/y741269430/Install-scRNAtoolVis/blob/main/png/2.png)  
### 6.去服务器找gfortran(https://blog.csdn.net/QFire/article/details/105250402)      
    ldconfig -p |grep fortran  
    ls /usr/lib/x86_64-linux-gnu/libgfortran* -lh  
### 7.添加软连接  
    sudo ln -s /lib/x86_64-linux-gnu/libgfortran.so.5 /usr/lib/x86_64-linux-gnu/libgfortran.so  
![4.png](https://github.com/y741269430/Install-scRNAtoolVis/blob/main/png/4.png)  
### 8.安装成功  
![3.png](https://github.com/y741269430/Install-scRNAtoolVis/blob/main/png/3.png)  

