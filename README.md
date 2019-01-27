# pyqt5-browser
  所用实验环境 ubuntu/trusty64
  
  vagrant init   ubuntu/trusty64
  
  将 Vagrantfile 里面 vb.gui = true 注释放开
```
   config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
     vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
   end
```

```
    1 sudo lsb_release -a
    2  sudo apt-get update
    #默认安装为 python3.5 改为 python3.4
    3  sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.4 70 --slave /usr/bin/python3m python3m /usr/bin/python3.4m
    #检测 python 版本
    4  python3 -V
    #安装插件
    5  sudo apt-get install python3-pyqt5
    6  python -V
    #在python3 环境下执行 import PyQt5 如果没有任何报错那么上述插件安装成功
    7  python3 
    >>> import PyQt5
    >>>
    #安装插件 python3-pyqt5.qtwebkit
    8  sudo apt-get install python3-pyqt5.qtwebkit
    #下载代码
    >>>
    9   git clone https://github.com/yetHandsome/pyqt5-browser.git
   10  ls
   11  cd pyqt5-browser
   12  clear
   13  ls
   #下面是安装图形界面
   14  sudo apt-get install xfce4
   15  sudo startxfce4&
   16  sudo apt-get install -y xfce4 virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11
   17  sudo VBoxClient-all
   18  sudo VBoxClient --clipboard
   19  sudo VBoxClient --draganddrop
   20  sudo VBoxClient --display
   21  sudo VBoxClient --checkhostversion
   22  sudo VBoxClient --seamless
   23  sudo startxfce4&
   #进入图形界面的2种方式
   #方式1
   sudo startx
   #方式2
   sudo init 5
   sudo init 6
   #在图形界面找到文件执行下面指令即可
   python3 my_browser.py
```
