# w4sp-lab
## 说明

把 w4sp-lab 修改了一下，官方提供的国内网络拉不起来🙃

**建议使用阿里云的 docker 镜像加速服务，因为我改好的基础镜像放在了阿里云上，这样比较快**

这里提供两种方法嗷😁



## 1、自己搭建

创建一个叫 w4sp-lab 的用户：
`useradd -m w4sp-lab -s /bin/bash -G sudo -U`

然后 `passwd w4sp-lab` 给这个用户设置密码

设置好密码之后，注销，使用 w4sp-lab 用户登录，把文件拷到虚拟机里面，然后 `sudo python w4sp_webapp.py` 就可以了

完事之后他应该不能自己打开 firefox 导致一些报错，不过不要紧，自己打开 firefox 然后输入 127.0.0.1:5000 访问就好了，不行的话多试几次😋



##  2、直接用虚拟机

如果不想自己配置，可以直接下载这个虚拟机😜

百度云链接：里面 w4sp-lab 文件夹有一个 parrot 虚拟机，账户名：w4sp-lab   密码：w4sp

root 用户的密码应该也是 root 来着？我忘记了🐷

https://pan.baidu.com/s/1u5EuRBKW-fOM1RkQVqh-xQ 
提取码：lggz



