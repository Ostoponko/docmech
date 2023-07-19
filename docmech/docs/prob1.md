# 在线文档无法加载图片？

1. 进入[ipaddress](https://www.ipaddress.com/)网站，查询 raw.githubusercontent.com 的IP地址。所列举的四个IPv4地址随便选取一个，比如下面列表的第一个。
    ```{ .yaml .copy }
    185.199.108.133
    185.199.109.133
    185.199.110.133
    185.199.111.133
    ```

2. 系统搜索 Windows PowerShell，输入 notepad 后 ++enter++ 打开记事本，点击打开，按照以下路径打开hosts文件：

    ``` { .yaml .copy }
    C:\windows\System32\drivers\etc\hosts
    ```

    <center>
    <img src="https://raw.githubusercontent.com/Ostoponko/Picstorage/master/JW%40%25W2(Y%5B1465%40IJY%24QQGG9.png"
    width="50%">
    <br>hosts文件路径
    </center>


3. 在最下面一行添加（无需 #）：
    ``` { .yaml .copy }
    185.199.108.133 raw.githubusercontent.com
    ```


4. 保存后 ++win+r++ 后输入 cmd，打开Command窗口，输入以下指令后 ++enter++ ：
    ``` { .yaml .copy }
    ipconfig/flushdns
    ```


5. 刷新完DNS解析之后，再次打开文档观察图片是否正常显示。


6. 如果本身访问github受限，可以试试科学上网。


7. 可以使用同学的电脑访问文档，或者阅读PDF版本。
