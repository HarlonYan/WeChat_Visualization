# 演示
![gif.gif](https://s2.loli.net/2025/02/01/iO4CzH8jNkZKuJU.gif)
![1.png](https://s2.loli.net/2025/02/01/DKyRgfXaslcP1uF.png)
![2.png](https://s2.loli.net/2025/02/01/fJmZ1GrUAuRjFwe.png)
![3.png](https://s2.loli.net/2025/02/01/tSaUJzv5TBXVn7W.png)
# 下载wechat_visualization压缩包
下载压缩包，解压到本地

# 使用软件下载聊天纪录元数据

使用“留痕”Memotrace软件，根据教程下载与某个人的聊天纪录（csv版本）

[Memo Trace软件官网](https://memotrace.cn/)

[github网址](https://github.com/LC044/WeChatMsg)

[教程](https://memotrace.cn/doc/)

替换掉文件夹中的 *聊天文本数据.csv* （文件命名一定要修改为*聊天文本数据*）

# 简单修改两处代码

打开压缩包中的*clean_data.py*，修改第60行的代码，*男生/女生的微信号* 修改为*聊天文本数据.csv* 中*Sender*一列中对应的值

如男生的微信号是wxid_8agcmdewxwebm12，女生的微信号是wxid_ks2r97efface24ra12，则将代码修改为如下

```
sender_dic = {'wxid_8agcmdewxwebm12':'Boy','wxid_ks2r97efface24ra12':'Girl'}
```



打开*main.py*，修改第101行代码。修改之前你首先需要注册SMMS图床账号

[SMMS官网](https://smms.app/)

注册完账号后，进入个人空间，获取api token，将其复制到"authorization"的后面，注意token要加引号

如api token为 Z1txoFcearzJacrereqfGCUlUaqHTHg8ac，则修改代码为

```
CONFIGS = {
    "url": "https://sm.ms/api/v2/upload",
    #修改为账号api token
    "authorization": "Z1txoFcearzJacrereqfGCUlUaqHTHg8ac",
}
```
![image-20250201223051019.png](https://s2.loli.net/2025/02/01/4P6HfGgwZVW52Rd.png)
![image-20250201223203403.png](https://s2.loli.net/2025/02/01/gAT5EBFonMUC4Qc.png)

# 一键运行代码

打开*main.py*运行。等待代码运行完成，结果会输出在output文件夹之中

![image-20250201223603947.png](https://s2.loli.net/2025/02/01/5nPQoVXqRG2TeMh.png)

# 下载Tableau

下载tableau desktop软件，可以下载public免费版本

[Tableau Desktop Public Edition](https://www.tableau.com/zh-cn/products/public/download)

填写一些信息后即可下载安装包，根据提示安装即可。

如果是学生的话，可以通过学生认证免费使用 Tableau Desktop。

使用tableau desktop 打开*可视化.twb*

第一次打开需要重新编辑数据链接：点击左下角数据源、以此点击左上角的连接数据，将其重新连接到output文件夹中对应的xlsx即可。

点击下面 仪表盘 即可看到数据的可视化结果。

![image-20250201224833518.png](https://s2.loli.net/2025/02/01/zit6bQp5ZA2scG3.png)
