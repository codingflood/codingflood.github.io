---

## title: 在Debian Linux上快速简单安装julia

---

如何在Debian Linux中快速简单的安装julia呢？
    
julia是没有简单的deb包的，不能通过终端直接apt-get install来安装。
    
那么我们有一个很简单方便的方法来使用它：
    
到官网上https://julialang.org/downloads/ 下载一个Generic Linux Binaries for x86包，根据你的电脑选择32还是64位的，如图：

![julia 安装包下载](/assets/img/juliapkg1.png/683x384)

下载下来之后，解压到你想放的位置：

![julia 安装](/assets/img/juliapkg2.png/683x384)


![julia 安装](/assets/img/juliapkg3.png/683x384)


![julia 安装](/assets/img/juliapkg4.png/683x384)

其中，julia可运行程序就在bin文件夹中：

![julia 安装](/assets/img/juliapkg5.png/683x384)

在这个时候，julia可以右键运行程序了，但是要在全局任何位置打开终端键入julia都可以运行的话还要做最后一个工作，打开终端键入：

'''
echo "alias julia='/path/to/install/folder/bin/julia'"  ~/.bashrc && source ~/.bashrc
'''

例如我的安装路径是/root/Julia/julia-1.0.0-linux-x86_64/julia-1.0.0/bin，那么我只要在终端中键入：

'''
echo "alias julia='/root/Julia/julia-1.0.0-linux-x86_64/julia-1.0.0/bin/julia'"  ~/.bashrc && source ~/.bashrc
'''
当然，其他方法还是有的，包括自己git下来然后make……但是我觉得这样最简便快速。

