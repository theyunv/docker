## 1 MarkDown
>排版工具。问题或建议，请留言。**[Markdown测试](#jump_8)**

### 1.1 Markdown是一种轻量级的「标记语言」。

###  1.2 TOC 
###1.1 全称为 Table of Content，列出全部标题。

[TOC]

由于app只支持到二级列表，本工具仅支持二级标题和三级标题的显示。

## 2 Markdown语法教程
### 2.1 标题

不同数量的`#`可以完成不同的标题(1-6级)，如下：
# 一级标题
## 二级标题
### 三级标题

### 2.2 字体
**这个是粗体** *这个是斜体* ***这个是粗体加斜体*** ~~这里想用删除线~~  
注：如果想给字体换颜色、字体或者居中显示，需要使用内嵌HTML来实现。

### 2.3 无序列表 有序列表
无序列表，在符号`-`后加空格使用。如果要控制列表的层级，则需要在符号`-`前使用空格
有序列表，在数字及符号`.`后加空格后输入内容。如下：
1. 有序列表 1
2. 有序列表 2
- 无序列表 1
- 无序列表 2
  - 无序列表 2.1
  - 无序列表 2.2

### 2.4 引用
引用的格式是在符号`>`后面书写文字。如下：
> 读一本好书，就是在和高尚的人谈话。 ——歌德  
> 雇用制度对工人不利，但工人根本无力摆脱这个制度。 ——阮一峰

### 2.5 链接

app公众号仅支持公众号文章链接，即域名为`https://mp.weixin.qq.com/`的合法链接。使用方法如下所示：

对于该论述，欢迎读者查阅之前发过的文章，[你是《未来世界的幸存者》么？](https://mp.weixin.qq.com/s/s5IhxV2ooX3JN_X416nidA)  
<a id="jump_8">Markdown测试跳转</a>

### 2.6 图片

插入图片，格式如下：
![这里写图片描述](https://zeromicro.github.io/go-zero-pages/resource/go-zero-practise.png)
支持 jpg、png、gif、svg 等图片格式，**其中 svg 文件仅可在xx公众平台中使用**，svg 文件示例如下：
![](https://markdown.com.cn/images/i-am-svg.svg)  
注：支持图片 ***拖拽和截图粘贴*** 到编辑器中，仅支持 https 的图片，图片粘贴到app时会自动上传app服务器。

### 2.7 分割线
可以在一行中用三个以上的减号来建立一个分隔线，同时需要在分隔线的上面空一行。如下：

---
### 2.8 表格

可以使用冒号来定义表格的对齐方式，如下：

| 姓名  | 年龄 |    工作 |
| :----- | :--: | -------: |
| 小可爱 | 18 | 吃可爱多 |
| 小小勇敢 | 20 | 爬棵勇敢树 |
| 小小小机智 | 22 | 看一本机智书 |

## 3. 特殊语法

### 3.1 脚注
脚注与链接的区别如下所示：

```markdown
链接：[文字](链接)
脚注：[文字](脚注解释 "脚注名字")
```

有人认为在[大前端时代](https://en.wikipedia.org/wiki/Front-end_web_development "Front-end web development")的背景下，移动端开发（Android、IOS）将逐步退出历史舞台。

[全栈工程师](是指掌握多种技能，并能利用多种技能独立完成产品的人。 "什么是全栈工程师")在业务开发流程中起到了至关重要的作用。

脚注内容请拉到最下面观看。

### 3.2 代码块

> 支持平台：app代码主题仅支持app公众号！其他主题无限制。

如果在一个行内需要引用代码，只要用反引号引起来就好，如下：

Use the `printf()` function.

在需要高亮的代码块的前一行及后一行使用三个反引号，同时**第一行反引号后面表示代码块所使用的语言**，如下：

```Golang
package main

import "fmt"

func main() {
    fmt.Println("Hello world") 
}
```

支持以下语言种类：

```
bash
clojure，cpp，cs，css
dart，dockerfile, diff
erlang
go，gradle，groovy
haskell
java，javascript，json，julia
kotlin
lisp，lua
makefile，markdown，matlab
objectivec
perl，php，python
r，ruby，rust
scala，shell，sql，swift
tex，typescript
verilog，vhdl
xml
yaml
```

如果想要更换代码高亮样式，可在上方**代码主题**中挑选。
有以下注意事项：

- 带行号且不换行，代码大小与官方一致
- 需要在代码块处标志语言，否则无法高亮
- 粘贴到xx公众号后，用鼠标点代码块内外一次，完成高亮

diff 不能同时和其他语言的高亮同时显示，且需要调整代码主题为app代码主题以外的代码主题才能看到 diff 效果，使用效果如下:
```diff
+ 新增项
- 删除项
```
**其他主题不带行号，可自定义是否换行，代码大小与当前编辑器一致**

### 3.3 数学公式

> 支持平台：app公众号、知乎。

行内公式使用方法，比如这个化学公式：${Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}$

块公式使用方法如下：

$$H(D_2) = -\left(\frac{2}{4}\log_2 \frac{2}{4} + \frac{2}{4}\log_2 \frac{2}{4}\right) = 1$$

矩阵：

$$
  \begin{pmatrix}
  1 & a_1 & a_1^2 & \cdots & a_1^n \\
  1 & a_2 & a_2^2 & \cdots & a_2^n \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  1 & a_m & a_m^2 & \cdots & a_m^n \\
  \end{pmatrix}
$$

公式由于app不支持，目前的解决方案是转成 svg 放到app中，无需调整，矢量不失真。

目前测试如果公式量过大，在 Chrome 下会存在粘贴后无响应，但是在 Firefox 中始终能够成功。

### 3.4 注音符号

> 支持平台：app公众号。

支持注音符号，用法如下：

Markdown Nice 这么好用，简直是{喜大普奔|hē hē hē hē}呀！

### 3.5 横屏滑动幻灯片

> 支持平台：app公众号。

通过`<![](url),![](url)>`这种语法设置横屏滑动滑动片，具体用法如下：

<![蓝1](https://markdown.com.cn/images/blue.jpg),![绿2](https://markdown.com.cn/images/green.jpg),![红3](https://markdown.com.cn.jpg)>

## 4 其他语法

### 4.1 HTML

支持原生 HTML 语法，请写内联样式，如下：

<span style="display:block;text-align:right;color:orangered;">橙色居右</span>
<span style="display:block;text-align:center;color:orangered;">橙色居中</span>

### 4.2 UML

不支持，推荐使用开源工具`https://draw.io/`制作后再导入图片


## 5 致谢

* 测试1 [test-fromat](https://www.baidu.com "灵感来源")
* 测试2 [Baidu](https://www.baidu.com "Baidu")

## 一、Docker入门

1. Docker是一个开源的引擎，可以轻松的为任何应用创建一个轻量级的、可移植的、自给自足的容器。开发者在笔记本上编译测试通过的容器可以批量地在生产环境中部署，
包括VMs（虚拟机）、 bare metal、OpenStack 集群和其他的基础应用平台。  
Docker诞生于 2013 年初，最初是 dotCloud 公司内部的一个业余项目。它基于 Google 公司推出的 Go 语言实现。 项目后来加入了 Linux 基金会，遵从了 Apache 2.0 协议，项目代码在 GitHub 上进行维护。Docker 项目的目标是实现轻量级的操作系统虚拟化解决方案。 Docker 的基础是 Linux 容器（LXC）等技术。
>Linux Container主要由Namespace 2 和Cgroups 3 两大机制来保证实现  
>Namespace命名空间主要用于资源的隔离（诞生于2002年）  
>Cgroups(Control Groups)就负责资源管理控制作用，比如进程组使用CPU/MEM的限制，进程组的优先级控制，进程组的挂起和恢复等等。（由Google贡献，2008年合并到了Linux Kernel）

- 文档地址 ：https://www.docker.org.cn/book/docker/docker-getting-started-14.html  
- 官方网站 ：https://docs.docker.com/linux/started/
- 参考文档1 ：https://dockertips.readthedocs.io/en/latest/docker-install.html
- 参考文档2 ：https://cloud.tencent.com/developer/article/2093710(Docker常用命令大全)

2. Docker系统有两个程序：docker服务端和docker客户端。其中docker服务端是一个服务进程，管理着所有的容器。docker客户端则扮演着docker服务端的远程控制器，可以用来控制docker的服务端进程。    
docker Version 查看版本  
3. Docker镜像：
- Docker image是一个 read-only 文件，这个文件包含文件系统，源码，库文件，依赖，工具等一些运行application所需要的文件
- 可以理解成一个模板，docker image具有分层的概念  
镜像都是按照 用户名/ 镜像名的方式来存储的，有一组比较特殊的镜像，比如ubuntu这类基础镜像，经过官方的验证，值得信任，可以直接用 镜像名来检索到  
docker search tutorial 搜索可用的docker镜像 (官方网址是：https://index.docker.io/)  
下载容器镜像 docker pull learn/tutorial  
4. Docker容器：“一个运行中的docker image”
- 实质是复制image并在image最上层加上一层 read-write 的层 （称之为 container layer ,容器层），基于同一个image可以创建多个container  
可以理解为在沙盒中运行的进程。这个沙盒包含了该进程运行所必须的资源，包括文件系统、系统类库、shell 环境等等。但这个沙盒默认是不会运行任何程序的。你需要在沙盒中运行一个进程来启动某一个容器。这个进程是该容器的唯一进程，所以当该进程结束的时候，容器也会完全的停止。  
在docker容器中运行hello world!： docker run learn/tutorial echo "hello word"  
5. 在容器中安装新的程序：docker run learn/tutorial apt-get install -y ping  
例如使用ubuntu的apt-get命令来安装ping程序： apt-get install -y ping  
在执行apt-get 命令的时候，要带上-y参数。如果不指定-y参数的话，apt-get命令会进入交互模式，需要用户输入命令来进行确认，但在docker环境中是无法响应这种交互的。
6. 保存对容器的修改，docker中保存状态的过程称之为committing，它保存的新旧状态之间的区别，从而产生一个新的版本。
- 6.1 首先获得安装完ping命令之后容器的id：docker ps -l，然后把这个镜像保存为learn/ping。   
6.1.1 运行docker commit，可以查看该命令的参数列表。  
6.1.2 你需要指定要提交保存容器的ID。(译者按：通过docker ps -l 命令获得)  
6.1.3 无需拷贝完整的id，通常来讲最开始的三至四个字母即可区分。（译者按：非常类似git里面的版本号)  
- 6.2 执行完docker commit命令之后，会返回新版本镜像的id号：docker commit dd720cea2fb5 learn/ping  
7. 运行新的镜像：docker run learn/ping /bin/sh -C && ping www.baidu.com  
- 提示：一定要使用新的镜像名 learn/ping来运行ping命令。(译者按：最开始下载的learn/tutorial镜像中是没有ping命令的)
8. 检查运行中的镜像  
docker ps -a 命令可以查看所有容器列表  
docker inspect 777192d9617b 命令我们可以查看更详细的关于某一个容器的信息
9. 发布docker镜像：例-把learn/ping镜像发布到docker的官方的索引网站。  
- 9.1 docker images命令可以列出所有安装过的镜像。
- 9.2 docker push命令可以将某一个镜像发布到官方网站：docker push learn/ping 。
- 9.3 你只能将镜像发布到自己的空间下面。这个模拟器登录的是learn帐号。

案例演示：将本地镜像推送到私有库
```shell
Docker Registry是官方提供的工具，可以用于构建私有镜像仓库
1、下载镜像Docker Registry
docker pull registry 
2、运行私有库Registry，相当于本地有个私有Docker hub
docker run -d -p 5000:5000  -v /zzyyuse/myregistry/:/tmp/registry --privileged=true registry
3、案例演示创建一个新镜像，centos安装ifconfig命令
3.1、从Hub上下载ubuntu镜像到本地并成功运行，并安装redis
docker pull centos
docker run -it centos /bin/bash
apt install -y redis
3.2、安装完成，提交镜像
docker commit -m="add test" -a="test" 846cde73b2fd centos1:1.0
3、验证私服上镜像
curl -XGET http://192.168.1.200:5000/v2/\_catalog
4、将新镜像centos1:1.0修改符合私服规范的Tag
docker tag centos1:1.0  192.168.1.200:5000/centos1:1.0
5、修改配置文件，支持http
docker默认不允许http方式推送镜像，通过配置选项来取消这个限制。
5.1、查看配置文件
cat /etc/docker/daemon.json
5.2、修改配置文件
vim /etc/docker/daemon.json
{
  "registry-mirrors": ["https://cmquykjm.mirror.aliyuncs.com"],
  "insecure-registries": ["192.168.2.200:5000"]
}
ip：自己启动服务器的ip
端口：映射的端口
5.3、修改之后查看配置并重新启动
PS：重新启动端口之后，需启动私有仓库
6、push到私有仓库
docker push 192.168.1.200:5000/centos1:1.0
7、验证私服镜像
curl -XGET http://192.168.1.200:5000/v2/\_catalog
8、pull到本地并运行
docker pull 192.168.1.200:5000/centos1:1.0
```

### 2.1使用官方安装脚本自动安装docker
```shell
curl -fsSL https://get.docker.com | bash -s docker --mirror Aliyun
systemctl enable docker
systemctl start docker
# 配置阿里云镜像
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://gr9o5vwc.mirror.aliyuncs.com"]
}
EOF
```
```shell
# sudo tee /etc/docker/daemon.json <<-'EOF'
# {
#   "registry-mirrors":[
#     "https://reg-mirror.qiniu.com",
#     "https://registry.docker-cn.com",
#     "https://hub-mirror.c.163.com",
#     "https://docker.mirrors.ustc.edu.cn"
#   ]
# }
# EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
sudo docker run hello-world
```
### 2.2安装docker-compose
```shell
curl -L "https://github.com/docker/compose/releases/download/2.14.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
# 或
curl -L https://get.daocloud.io/docker/compose/releases/download/v2.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```
#### 2.3 镜像的基本操作
> Docker中的镜像分层，支持通过扩展现有镜像，创建新的镜像。类似Java继承于一个Base基础类，自己再按需扩展。

> 新镜像是从 base 镜像一层一层叠加生成的。每安装一个软件，就在现有镜像的基础上增加一层
##### 2.3.1 帮助类启动命令
```shell
启动docker： systemctl start docke
停止docker： systemctl stop docke
重启docker： systemctl restart docke
查看docker状态： systemctl status docke
开机启动： systemctl enable docke
查看docker概要信息： docker info
查看docker总体帮助文档： docker --help
查看docker命令帮助文档： docker 具体命令 --help
```
##### 2.3.2、镜像命令
```shell
1.列出本地主机上的镜像docker images
REPOSITORY：表示镜像的仓库源
TAG：镜像的标签版本号
IMAGE ID：镜像ID
CREATED：镜像创建时间
SIZE：镜像大小
2.搜索镜像docker search [OPTIONS] 镜像名字
2.1 --limit  只列出N个镜像: 默认25个docker search --limit 5 redis
2.2 要查看所有镜像，包括未使用的镜像docker images --all或者docker images -a
查看镜像的版本https://hub.docker.com/搜索后点击Tags
3.拉取镜像docker pull 镜像名字:TAG没有TAG就是最新版,等价于：docker pull 镜像名字:latest
4.查看镜像 docker system df 查看镜像/容器/数据卷所占的空间
5、删除镜像 docker rmi 某个XXX镜像名字ID
5.1、删除单个 docker rmi  -f 镜像ID
5.2、删除多个 docker rmi -f 镜像名1:TAG 镜像名2:TAG 
5.3、删除全部 docker rmi -f $(docker images -qa)
6.虚悬镜像是什么？仓库名、标签都是<none>的镜像，俗称虚悬镜像dangling image
删除空悬镜像docker rmi $(docker images -f "dangling=true" -q)
7.docker commit提交容器副本使之成为一个新的镜像
docker commit -m="提交的描述信息" -a="作者" 容器ID 要创建的目标镜像名:标签名
(例：docker commit -m="add vim cmd" -a="test" c7f841ff540c centos1:1.0)
创建镜像:1、从已经创建的容器中更新镜像，并且提交这个镜像2、使用 Dockerfile 指令来创建一个新的镜像
8.将新镜像修改符合私服规范的Tag
docker   tag   镜像:Tag   Host:Port/Repository:Tag
(例：docker tag centos1:1.0  192.168.130.132:5000/centos1:1.0)
9.镜像的导出和导入 (offline)
docker image save nginx:1.20.0 -o nginx.tar
docker image load -i .\nginx.tar
docker export <CONTAINER ID > > my_container.tar 
docker import [options] my_container.tar [REPOSITORY[:TAG]]
```
>同一仓库源可以有多个 TAG版本，代表这个仓库源的不同个版本，我们使用 REPOSITORY:TAG 来定义不同的镜像。  
>如果你不指定一个镜像的版本标签，例如你只使用 ubuntu，docker 将默认使用 ubuntu:latest 镜像

>docker save和docker export的区别
>对于Docker Save方法，会保存该镜像的所有历史记录
>对于Docker Export 方法，不会保留历史记录，即没有commit历史
>docker save保存的是镜像（image），docker export保存的是容器（container）；
>docker load用来载入镜像包，docker import用来载入容器包，但两者都会恢复为镜像；
>docker load不能对载入的镜像重命名，而docker import可以为镜像指定新名称。

##### 2.3.3 新建+启动命令
```shell
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
 OPTIONS说明（常用）：有些是一个减号，有些是两个减号
--name="容器新名字"       为容器指定一个名称；
-d: 后台运行容器并返回容器ID，也即启动守护式容器(后台运行)；
-i：以交互模式运行容器，通常与 -t 同时使用；
-t：为容器重新分配一个伪输入终端，通常与 -i 同时使用；也即启动交互式容器(前台有伪终端，等待交互)；
-P: 随机端口映射，大写P----P hostPort:containerPort
-p: 指定端口映射，小写p
-p hostPort:containerPort 端口映射 -p 8080:80
-p ip:hostPort:containerPort 配置监听地址 -p 10.0.0.1:8080:80
-p ip::containerPort 随机分配端口 -p 10.0.0.1::80
-p hostPort:containerPort:udp 指定协议 -p 8080:80:tcp
-p 81:80 -p 443:443 指定多个
--rm：容器退出时自动清理容器内部的文件系统。
-h HOSTNAME 或者 --hostname=HOSTNAME： 设定容器的主机名，它会被写到容器内的 /etc/hostname 和 /etc/hosts。
--dns=IP_ADDRESS： 添加 DNS 服务器到容器的 /etc/resolv.conf 中，让容器用这个服务器来解析所有不在 /etc/hosts 中的主机名。
--dns-search=DOMAIN： 设定容器的搜索域，当设定搜索域为 .example.com 时，在搜索一个名为 host 的主机时，DNS 不仅搜索 host，还会搜索 host.example.com。
(例docker run -it --rm -h host_ubuntu  --dns=114.114.114.114 --dns-search=test.com ubuntu)
--network多个容器连接到同一个网络后可以相互ping通（已安装ping）
```
>创建一个容器并进入交互式模式
>docker run -it centos /bin/bash  
>参数说明：  
>-i: 交互式操作。  
>-t: 终端。  
>centos : centos 镜像。  
>/bin/bash：放在镜像名后的是命令，这里我们希望有个交互式 Shell，因此用的是 /bin/bash。  
>要退出终端，直接输入 exit；
##### 2.3.4 docker创建和删除网络
```shell
2.3.4.1 列出所有Docker网络
docker network ls
查看容器连接的网络
docker network inspect my_network
2.3.4.2 创建Docker网络
Docker提供了多种网络驱动程序（如bridge、host、overlay等）根据需求选择合适的驱动程序来创建网络。
1. 创建默认的桥接网络
docker network create my_network
2. 创建自定义桥接网络
docker network create --driver bridge --subnet 192.168.1.0/24 --gateway 192.168.1.1 my_custom_network
参数说明：
--driver bridge：指定使用桥接网络驱动。
--subnet 192.168.1.0/24：指定子网范围。
--gateway 192.168.1.1：指定网关地址。
--my_custom_network：网络名称。
3. 创建主机网络
主机网络（host）允许容器直接使用宿主机的网络栈。这种网络类型适用于需要高性能网络通信的场景。
docker network create --driver host my_host_network
参数说明：
--driver host：指定使用主机网络驱动。
--my_host_network：网络名称。
4. 创建覆盖网络
覆盖网络（overlay）适用于多主机环境，允许不同主机上的容器之间进行通信。
docker network create --driver overlay my_overlay_network
参数说明：
--driver overlay：指定使用覆盖网络驱动。
--my_overlay_network：网络名称。
5. 将容器连接到网络
5.1 在创建容器时连接到网络。
docker run -d --name my_container --network my_network nginx
5.2 将已运行的容器连接到网络
docker network connect my_network my_container
5.3 将容器从网络中移除
docker network disconnect my_network my_container
2.3.4.3 删除Docker网络
删除网络之前，确保没有容器依赖于它，需要检查特定网络上的容器，在输出中，查找Containers字段。如果这个字段列出了任何容器，那么在删除网络之前，你需要先停止并删除这些容器。 
docker network inspect my_network
删除指定的Docker网络
docker network rm my_network
删除多个网络
docker network rm network1 network2
删除所有未使用的网络
docker network prune
```

#### 2.4 容器的基本操作
```shell
2.4.1 容器的列出(up) | docker container ls | docker ps
-a :显示所有的容器，包括未运行的。
-f :根据条件过滤显示的内容。
--format :指定返回值的模板文件。
-l :显示最近创建的容器。
-n :列出最近创建的n个容器。
--no-trunc :不截断输出。
-q :静默模式，只显示容器编号。  
-s :显示总的文件大小。
```
2.4.2 退出容器
```shell
1、exit退出
run进去容器，exit退出，容器停止
2、ctrl+p+q
run进去容器，ctrl+p+q退出，容器不停止
2.4.3 启动已停止运行的容器
docker start 容器ID或者容器名
2.4.4 重启容器
docker restart 容器ID或者容器名
2.4.5 停止容器
docker stop 容器ID或者容器名
2.4.6 强制停止容器
docker kill 容器ID或容器名
2.4.7 删除已停止的容器
docker rm 容器ID
一次性删除多个容器实例
docker rm -f $(docker ps -a -q)
docker ps -a -q | xargs docker rm
docker ps -a -q：查询进行的容器ID
2.4.8 查看容器日志docker logs 容器ID  (PS：容器ID可省略为前三位)
2.4.9 查看容器内运行的进程docker top 容器ID
2.4.10 查看容器内部细节docker inspect 容器ID
2.4.11 进入容器内部docker exec -it 容器ID bashShell 例：docker exec -it redis /bin/bash
2.4.12 使用attach进入容器docker attach 容器ID
2.4.13 查看容器端口的映射情况docker port 1692945642a4 或 docker port redis
2.4.14 为镜像添加一个新的标签docker tag 1692945642a4 redis:dev
```
> exec和attach两者的区别
> attach 直接进入容器启动命令的终端，不会启动新的进程，用exit退出，会导致容器的停止。
> exec 是在容器中打开新的终端，并且可以启动新的进程，用exit退出，不会导致容器的停止（推荐使用）。

#### 2.5 容器内文件拷贝
```shell
2.5.1 从容器内拷贝文件到主机上
docker cp  容器ID:容器内路径 目的主机路径 （ 例docker cp 306xxx:a.txt a.txt）
2.5.2 从宿主机拷贝文件到容器
docker cp 宿主机目录 容器ID:容器内目录（ 例docker cp a.txt 306xxx:a.txt）
```
#### 2.6 导入和导出容器
```shell
2.6.1 导出容器
export 导出容器的内容留作为一个tar归档文件对应import命令
docker export 容器ID > 文件名.tar
(例 docker export 3065f084c80d > centos.tar.gz)
2.6.2 导入容器
import 从tar包中的内容创建一个新的文件系统再导入为镜像对应export
cat 文件名.tar | docker import - 镜像用户/镜像名:镜像版本号
（例 cat centos.tar.gz | docker import - test/centos:8.8）将快照文件 ubuntu.tar.gz 导入到镜像 test/centos:8.8
指定 URL 或者某个目录来导入docker import http://example.com/exampleimage.tgz example/imagerepo
```
#### 2.7 Docker仓库管理
登录和退出
docker login
docker logout

| 命令  | 英文 |    中文 |
| :----- | :--- | :------ |
| attach | Attach to a running container | 当前 shell 下 attach 连接指定运行镜像 |
| build | Build an image from a Dockerfile | 通过 Dockerfile 定制镜像 |
| commit | Create a new image from a container changes | 提交当前容器为新的镜像 |
| cp | Copy files/folders from the containers filesystem to the host path | 容器中拷贝指定文件或者目录到宿主机中 |
| create | Create a new container | 创建一个新的容器，同 run，但不启动容器 |
| diff | Inspect changes on a container's filesystem | 查看 docker 容器变化 |
| events | Get real time events from the server | 从 docker 服务获取容器实时事件 |
| exec | Run a command in an existing container | 在已存在的容器上运行命令 |
| export | Stream the contents of a container as a tar archive |导出容器的内容流作为一个 tar 归档文件对应 import |
| history | Show the history of an image | 展示一个镜像形成历史 |
| images | List images | 列出系统当前镜像 |
| import | Create a new filesystem image from the contents of a tarball | 从tar包中的内容创建一个新的文件系统映像对应export |
| info | Display system-wide information | 显示系统相关信息 |
| inspect | Return low-level information on a container | 查看镜像/容器详细信息 |
| kill | Kill a running container | kill 指定 docker 容器 |
| load | Load an image from a tar archive | 从一个 tar 包中加载一个镜像对应 save |
| login | Register or Login to the docker registry server |注册或者登陆一个 docker 源服务器 |
| logout | Log out from a Docker registry server | 从当前 Docker registry 退出 |
| logs | Fetch the logs of a container | 输出当前容器日志信息 |
| port | Lookup the public-facing port which is NAT-ed to PRIVATE_PORT | 查看映射端口对应的容器内部源端口 |
| pause | Pause all processes within a container | 暂停容器 |
| ps |List containers | 列出容器列表 |

### 3.1 Dockerfile
Dockerfile是一个用来构建镜像的文本文件，文本内容包含了一条条构建镜像所需的指令和说明
```shell
FROM：定制的镜像都是基于 FROM 的镜像
RUN：用于执行后面跟着的命令行命令。有以下俩种格式：shell 格式,exec 格式
RUN <命令行命令>
# <命令行命令> 等同于，在终端操作的 shell 命令。
RUN ["可执行文件", "参数1", "参数2"]
# 例如：RUN ["./test.py", "dev", "offline"] 等价于 RUN ./test.py dev offline
```
>注意：Dockerfile 的指令每执行一次都会在 docker 上新建一层。所以过多无意义的层，会造成镜像膨胀过大。优化方式：\ && 连接shell语句
开始构建镜像
docker build -t usercenterrpc:v1 -f user/rpc/Dockerfile .
. 是上下文路径,是指 docker 在构建镜像，有时候想要使用到本机的文件（比如复制），docker build 命令得知这个路径后，会将路径下的所有内容打包。
>解析：由于 docker 的运行模式是 C/S。我们本机是 C，docker 引擎是 S。实际的构建过程是在 docker 引擎下完成的，所以这个时候无法用到我们本机的文件。这就需要把我们本机的指定目录下的文件一起打包提供给 docker 引擎使用。
>如果未说明最后一个参数，那么默认上下文路径就是 Dockerfile 所在的位置。
>注意：上下文路径下不要放无用的文件，因为会一起打包发送给 docker 引擎，如果文件过多会造成过程缓慢。
```shell
指令详解
3.1.1 COPY：复制指令
COPY [--chown=<user>:<group>] <源路径1>...  <目标路径>
COPY [--chown=<user>:<group>] ["<源路径1>",...  "<目标路径>"]
<源路径>：源文件或者源目录
<目标路径>：容器内的指定路径，该路径不用事先建好，路径不存在的话，会自动创建
```
```shell
3.1.2 ADD：和COPY 的使用格类似（同样需求下，官方推荐使用 COPY），不同之处如下：
ADD 的优点：在执行 <源文件> 为 tar 压缩文件的话，压缩格式为 gzip, bzip2 以及 xz 的情况下，会自动复制并解压到 <目标路径>。
ADD 的缺点：在不解压的前提下，无法复制 tar 压缩文件。会令镜像构建缓存失效，从而可能会令镜像构建变得比较缓慢。具体是否使用，可以根据是否需要自动解压来决定。
```
```shell
3.1.3 CMD类似于 RUN 指令，用于运行程序，但二者运行的时间点不同:
CMD 在docker run 时运行。
RUN 是在 docker build。
作用：为启动的容器指定默认要运行的程序，程序运行结束，容器也就结束。CMD 指令指定的程序可被 docker run 命令行参数中指定要运行的程序所覆盖。
注意：如果 Dockerfile 中如果存在多个 CMD 指令，仅最后一个生效。
格式：
CMD <shell 命令> 
CMD ["<可执行文件或命令>","<param1>","<param2>",...] 
CMD ["<param1>","<param2>",...]  # 该写法是为 ENTRYPOINT 指令指定的程序提供默认参数
```
```shell
ENTRYPOINT：类似于 CMD 指令，但其不会被 docker run 的命令行参数指定的指令所覆盖，而且这些命令行参数会被当作参数送给 ENTRYPOINT 指令指定的程序。
注意：如果 Dockerfile 中如果存在多个 ENTRYPOINT 指令，仅最后一个生效。如果运行 docker run 时使用了 --entrypoint 选项，将覆盖 ENTRYPOINT 指令指定的程序
格式：ENTRYPOINT ["<executeable>","<param1>","<param2>",...]
示例：假设已通过 Dockerfile 构建了 nginx:test 镜像：
FROM nginx

ENTRYPOINT ["nginx", "-c"] # 定参
CMD ["/etc/nginx/nginx.conf"] # 变参 

1、不传参运行docker run  nginx:test
容器内会默认运行以下命令，启动主进程。nginx -c /etc/nginx/nginx.conf
2、传参运行docker run  nginx:test -c /etc/nginx/new.conf
容器内会默认运行nginx -c /etc/nginx/new.conf，启动主进程(/etc/nginx/new.conf:假设容器内已有此文件)
```
```shell
3.1.4 ENV 设置环境变量，那么在后续的指令中，就可以使用这个环境变量
格式：
ENV <key> <value>
ENV <key1>=<value1> <key2>=<value2>...

示例：
ENV NODE_VERSION 7.2.0

RUN curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz"
```
```shell
3.1.5 ARG：构建参数，与 ENV 作用一致。不过作用域不一样。ARG 设置的环境变量仅对 Dockerfile 内有效，也就是说只有docker build 的过程中有效，构建好的镜像内不存在此环境变量。
构建命令 docker build 中可以用 --build-arg <参数名>=<值> 来覆盖。

格式：ARG <参数名>[=<默认值>]
```
```shell
3.1.6 VOLUME：定义匿名数据卷。在启动容器时忘记挂载数据卷，会自动挂载到匿名卷。
作用：避免重要的数据，因容器重启而丢失，这是非常致命的。避免容器不断变大。
格式：
VOLUME ["<路径1>", "<路径2>"...]
VOLUME <路径>
在启动容器 docker run 的时候，我们可以通过 -v 参数修改挂载点。
```
```shell
3.1.7 EXPOSE
仅仅只是声明端口
作用：帮助镜像使用者理解这个镜像服务的守护端口，以方便配置映射。
在运行时使用随机端口映射时，也就是 docker run -P 时，会自动随机映射EXPOSE的端口。
格式：EXPOSE <端口1> [<端口2>...]
```
```shell
3.1.8 WORKDIR指定工作目录。用 WORKDIR 指定的工作目录，会在构建镜像的每一层中都存在。以后各层的当前目录就被改为指定的目录，如该目录不存在，WORKDIR 会帮你建立目录。
docker build 构建镜像过程中的，每一个 RUN 命令都是新建的一层。只有通过 WORKDIR 创建的目录才会一直存在。
格式：WORKDIR <工作目录路径>
```
```shell
3.1.9 USER
用于指定执行后续命令的用户和用户组，这边只是切换后续命令执行的用户（用户和用户组必须提前已经存在）。
格式：USER <用户名>[:<用户组>]
```
```shell
3.2.0 HEALTHCHECK：用于指定某个程序或者指令来监控 docker 容器服务的运行状态。
格式：
HEALTHCHECK [选项] CMD <命令>：设置检查容器健康状况的命令
HEALTHCHECK NONE：如果基础镜像有健康检查指令，使用这行可以屏蔽掉其健康检查指令
HEALTHCHECK [选项] CMD <命令> : 这边 CMD 后面跟随的命令使用，可以参考 CMD 的用法。
```
```shell
3.2.1 ONBUILD：用于延迟构建命令的执行。简单的说，就是 Dockerfile 里用 ONBUILD 指定的命令，在本次构建镜像的过程中不会执行（假设镜像为 test-build）。当有新的 Dockerfile 使用了之前构建的镜像 FROM test-build ，这时执行新镜像的 Dockerfile 构建时候，会执行 test-build 的 Dockerfile 里的 ONBUILD 指定的命令。
格式：ONBUILD <其它指令>
```
```shell
3.2.2 LABEL：用来给镜像添加一些元数据（metadata），以键值对的形式，语法格式如下：
LABEL <key>=<value> <key>=<value> <key>=<value> ...
例如我们可以添加镜像的作者：LABEL org.opencontainers.image.authors="test"
```
### 3.2 Docker Compose
Compose 是用于定义和运行多容器 Docker 应用程序的工具。通过 Compose，您可以使用 YML 文件来配置应用程序需要的所有服务。然后，使用一个命令，就可以从 YML 文件配置中创建并启动所有服务。

#### 3.2.1 Compose 使用的三个步骤：
1.使用 Dockerfile 定义应用程序的环境。
2.使用 docker-compose.yml 定义构成应用程序的服务，这样它们可以在隔离环境中一起运行。
3.执行 docker-compose up 命令来启动并运行整个应用程序。
#### 3.2.2 安装 
```shell
1. curl -L https://get.daocloud.io/docker/compose/releases/download/v2.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose 或
curl -L "https://github.com/docker/compose/releases/download/v2.14.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
2. 将可执行权限应用于二进制文件：
sudo chmod +x /usr/local/bin/docker-compose
3. 创建软链：
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
测试是否安装成功
docker-compose version
```
#### 3.2.2 使用 
##### 3.2.2.1创建 Dockerfile 文件
```shell
FROM python:3.7-alpine AS builder
WORKDIR /code
ENV FLASK_APP app.py
ENV FLASK_RUN_HOST 0.0.0.0
RUN apk add --no-cache gcc musl-dev linux-headers
COPY requirements.txt requirements.txt
#COPY --from=builder /usr/share/zoneinfo/Asia/Shanghai /usr/share/zoneinfo/Asia/Shanghai
RUN pip install -r requirements.txt
COPY . .
CMD ["flask", "run"]

Dockerfile 内容解释：
FROM python:3.7-alpine: 从 Python 3.7 映像开始构建镜像。
WORKDIR /code: 将工作目录设置为 /code。
ENV FLASK_APP app.py
ENV FLASK_RUN_HOST 0.0.0.0
设置 flask 命令使用的环境变量。

RUN apk add --no-cache gcc musl-dev linux-headers: 安装 gcc，以便诸如 MarkupSafe 和 SQLAlchemy 之类的 Python 包可以编译加速。
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
复制 requirements.txt 并安装 Python 依赖项。

COPY . .: 将 . 项目中的当前目录复制到 . 镜像中的工作目录。--from指定来源之前的镜像别名
CMD ["flask", "run"]: 容器提供默认的执行命令为：flask run。
```
##### 3.2.2.2创建 docker-compose.yml
```shell
# yaml 配置
version: '3'
services:
  web:
    build: .
    ports:
     - "5000:5000"
  redis:
    image: "redis:alpine"

docker-compose.yml 内容解释：
该 Compose 文件定义了两个服务：web 和 redis。

web：该 web 服务使用从 Dockerfile 当前目录中构建的镜像。然后，它将容器和主机绑定到暴露的端口 5000。此示例服务使用 Flask Web 服务器的默认端口 5000 。
redis：该 redis 服务使用 Docker Hub 的公共 Redis 映像。
```
##### 3.2.2.2使用 Compose 命令构建和运行您的应用

docker-compose up 想在后台执行该服务可以加上 -d 参数

#### 3.3 yml 配置指令参考
```shell
3.3.1 version：指定本 yml 依从的 compose 哪个版本制定的。
3.3.2 build：指定为构建镜像上下文路径：
例如 webapp 服务，指定为从上下文路径 ./dir/Dockerfile 所构建的镜像：
version: "3.7"
services:
  webapp:
    build: ./dir
或者，作为具有在上下文指定的路径的对象，以及可选的 Dockerfile 和 args：
3.3.3 context：上下文路径。
3.3.4 dockerfile：指定构建镜像的 Dockerfile 文件名。
3.3.5 args：添加构建参数，这是只能在构建过程中访问的环境变量。
3.3.6 labels：设置构建镜像的标签。为容器添加Docker元数据（metadata）信息
3.3.7 target：多层构建，可以指定构建哪一层。

version: "3.7"
services:
  webapp:
    build:
      context: ./dir
      dockerfile: Dockerfile-alternate
      args:
        buildno: 1
      labels:
        - "com.example.description=Accounting webapp"
        - "com.example.department=Finance"
        - "com.example.label-with-empty-value"
      target: prod
3.3.8 cap_add，cap_drop
添加或删除容器拥有的宿主机的内核功能。
cap_add:
  - ALL # 开启全部权限
cap_drop:
  - SYS_PTRACE # 关闭 ptrace权限
3.3.9 cgroup_parent 为容器指定父 cgroup 组，意味着将继承该组的资源限制。
cgroup_parent: m-executor-abcd
3.3.10 command覆盖容器启动的默认命令。
command: ["bundle", "exec", "thin", "-p", "3000"]
3.3.11 container_name 指定自定义容器名称，而不是生成的默认名称。
container_name: my-web-container
3.3.12 depends_on设置依赖关系。
docker-compose up ：以依赖性顺序启动服务。在以下示例中，先启动 db 和 redis ，才会启动 web。
docker-compose up SERVICE ：自动包含 SERVICE 的依赖项。在以下示例中，docker-compose up web 还将创建并启动 db 和 redis。
docker-compose stop ：按依赖关系顺序停止服务。在以下示例中，web 在 db 和 redis 之前停止。
version: "3.7"
services:
  web:
    build: .
    depends_on:
      - db
      - redis
  redis:
    image: redis
  db:
    image: postgres
注意：web 服务不会等待 redis db 完全启动 之后才启动。
docker-compose up -d 【执行yml文件，创建并启动容器】进入docker-compose对应的文件目录下，构建并后台启动
docker-compose down  【关闭并删除容器】
docker-compose stop  【关闭】
docker-compose start  【启动】
docker-compose restart  【重新启动】
docker-compose logs -f  【查看日志】
3.3.13 deploy 指定与服务的部署和运行有关的配置。只在 swarm 模式下才会有用。
version: "3.7"
services:
  redis:
    image: redis:alpine
    deploy:
      mode：replicated
      replicas: 6
      endpoint_mode: dnsrr
      labels: 
        description: "This redis service label"
      resources:
        limits:
          cpus: '0.50'
          memory: 50M
        reservations:
          cpus: '0.25'
          memory: 20M
      restart_policy:
        condition: on-failure
        delay: 5s
        max_attempts: 3
        window: 120s
可以选参数：
endpoint_mode：访问集群服务的方式。
endpoint_mode: vip 
# Docker 集群服务一个对外的虚拟 ip。所有的请求都会通过这个虚拟 ip 到达集群服务内部的机器。
endpoint_mode: dnsrr
# DNS 轮询（DNSRR）。所有的请求会自动轮询获取到集群 ip 列表中的一个 ip 地址。
labels：在服务上设置标签。可以用容器上的 labels（跟 deploy 同级的配置） 覆盖 deploy 下的 labels。
mode：指定服务提供的模式。
replicated：复制服务，复制指定服务到集群的机器上。
global：全局服务，服务将部署至集群的每个节点。
restart_policy：配置如何在退出容器时重新启动容器。
rollback_config：配置在更新失败的情况下应如何回滚服务。
update_config：配置应如何更新服务，对于配置滚动更新很有用。
3.3.14 devices 指定设备映射列表。
devices:
  - "/dev/ttyUSB0:/dev/ttyUSB0"
3.3.15 dns
自定义 DNS 服务器，可以是单个值或列表的多个值。
dns: 8.8.8.8
或
dns:
  - 8.8.8.8
  - 9.9.9.9
3.3.16 dns_search  自定义 DNS 搜索域。可以是单个值或列表。
dns_search: example.com
或
dns_search:
  - dc1.example.com
  - dc2.example.com
3.3.17 entrypoint 覆盖容器默认的 entrypoint。
entrypoint: /code/entrypoint.sh
也可以是以下格式：
entrypoint:
    - php
    - -d
    - zend_extension=/usr/local/lib/php/extensions/no-debug-non-zts-20100525/xdebug.so
    - -d
    - memory_limit=-1
    - vendor/bin/phpunit
例：docker run --rm -it --entrypoint sh fdf23d7683de 查看和进入镜像内部
3.3.18 env_file从文件添加环境变量。可以是单个值或列表的多个值。
env_file: .env
也可以是列表格式：
env_file:
  - ./common.env
  - ./apps/web.env
  - /opt/secrets.env
3.3.19 environment 添加环境变量。您可以使用数组或字典、任何布尔值，布尔值需要用引号引起来，以确保 YML 解析器不会将其转换为 True 或 False。
environment:
  RACK_ENV: development
  - RACK_ENV=development
  SHOW: 'true'
  TZ: Asia/Shanghai # 时区上海 - Time zone Shanghai (Change if needed)
3.3.20 expose 暴露端口，但不映射到宿主机，只被连接的服务访问。
仅可以指定内部端口为参数：
expose:
 - "3000"
 - "8000"
3.3.21 extra_hosts 添加主机名映射。类似 docker client --add-host。
extra_hosts:
 - "somehost:162.242.195.82"
 - "otherhost:50.31.209.229"
以上会在此服务的内部容器中 /etc/hosts 创建一个具有 ip 地址和主机名的映射关系：
162.242.195.82  somehost
50.31.209.229   otherhost
3.3.22 healthcheck
用于检测 docker 服务是否健康运行
healthcheck:
  test: ["CMD", "curl", "-f", "http://localhost"] # 设置检测程序
  interval: 1m30s # 设置检测间隔
  timeout: 10s # 设置检测超时时间
  retries: 3 # 设置重试次数
  start_period: 40s # 启动后，多少秒开始启动检测程序
3.2.23 image 指定容器运行的镜像。以下格式都可以：
image: redis
image: ubuntu:14.04
image: tutum/influxdb
image: example-registry.com:4000/postgresql
image: a4bc65fd # 镜像id
3.3.24 logging 服务的日志记录配置。
driver：指定服务容器的日志记录驱动程序，默认值为json-file。有以下三个选项
driver: "json-file"
driver: "syslog"
driver: "none"
仅在 json-file 驱动程序下，可以使用以下参数，限制日志得数量和大小。
logging:
  driver: json-file
  options:
    max-size: "200k" # 单个文件大小为200k
    max-file: "10" # 最多10个文件
当达到文件限制上限，会自动删除旧得文件。
syslog 驱动程序下，可以使用 syslog-address 指定日志接收地址。
logging:
  driver: syslog
  options:
    syslog-address: "tcp://192.168.0.42:123"
3.3.25 network_mode 设置容器的网络模式。
默认情况下docker-compose会建立一个默认的网络，名称为docker-compose.yml所在目录名称myappdir小写形式加上"_default"，例如"myappdir_default"。
这个默认网络会对所有services下面的服务生效，所以services下面的各个服务之间才能够通过service名称互相访问。
network_mode: "bridge"
network_mode: "host" #容器环境不隔离，将使用主机的端口和ip，不能与ports端口映射同时使用
network_mode: "none"
network_mode: "service:[service name]"
network_mode: "container:[container name/id]"
networks ：配置容器连接的网络，引用顶级 networks 下的条目 。
aliases ：同一网络上的其他容器可以使用服务名称或此别名来连接到对应容器的服务。
services:
  some-service:
    networks:
      some-network:
        aliases:
         - alias1
      other-network:
        aliases:
         - alias2
networks:
  some-network:
    # Use a custom driver
    driver: custom-driver-1
  other-network:
    # Use a custom driver which takes special options
    driver: custom-driver-2
some-service这个容器会加入到网络中，并且在网络中的名称为：some-service。
多个容器，不在相同的配置中，也会有网络通讯的需求 。那么就可以使用公共的网络配置，通过docker network create创建好的网络，
而不是让docker-compose创建一个新的，这个时候就需要用到“external”关键字了。
指定了some-service特殊网络，所以default默认网络就自动失效了，如果需要使用default网络需要显性地指定下。
networks:
  default:
    driver: bridge
  some-service:
    external:
      name: bridge2
示例：docker-compose配置networks
3.3.25.1 默认网络
例如, 假设有一个项目，目录名myapp, docker-compose.yml 配置如下:
version: "3"
services:
  web:
    build: .
    ports:
      - "8000:8000"
  db:
    image: postgres
    ports:
      - "8001:5432"
当执行 docker-compose up 的时候。会发生以下事情：
会创建一个名字是 myapp_default的网络（networks）
web这个容器会加入到 myapp_default网络中，并且在网络中的名称为：web 。
db这个容器会加入到 myapp_default网络中，并且在网络中的名称为：db。
这里，每个容器都能通过应用名找到对方，例如，web容器可以通过 postgres://db:5432 来使用 Pg数据库。

上面例子还有一个注意点就是端口号，注意区分HOST_PORT和CONTAINER_PORT，以上面的db为例：
8001 是宿主机的端口
5432（postgres的默认端口） 是容器的端口
当容器之间通讯时 ， 是通过 CONTAINER_PORT 来连接的。这里有宿主机端口，那么容器就可以通过宿主机端口和外部应用连接。  
更新容器：对已经启动的容器，再执行 docker-compose up 的时候，旧容器删除，然后创建一个新的容器。
新容器会加入到网络，相同的网络名称，但容器IP是不一样的。已经连接的其他容器会自己重连到新的容器IP上。

3.3.25.2 自定义网络
可能通过一级配置networks来自定义网络，可以创建更复杂的网络选项和配置，也可以用来连接已经存在的网络（不是通过compose创建的）
每个service 配置下也可以指定networks配置，来指定一级配置的网络。
例如：
version: "3"
services:

  proxy:
    build: ./proxy
    networks:
      - frontend
  app:
    build: ./app
    networks:
      - frontend
      - backend
  db:
    image: postgres
    networks:
      - backend
  testsrv:
    image: testsrv
    networks: #每一次 down,up 都会生成新的IP,在docker-compose中固定容器testsrv的ip
      test_net:
            ipv4_address: 172.20.0.2 # testsrv的内部ip地址就固定住了,# 保留 172.20.0.1 作为test_net的网关ip
networks:
  frontend:
    # Use a custom driver
    driver: custom-driver-1
  backend:
    # Use a custom driver which takes special options
    driver: custom-driver-2
    driver_opts:
      foo: "1"
      bar: "2"
  test_net:
    driver: bridge
    ipam:
      config:
        - subnet: 172.20.0.0/16 # 子网

一级配置networks 用来创建自定义的网络 。这里配置了两个frontend和backend . 且自定义了网络类型。
每一个serviceg下，proxy , app , db都定义了一下networks配置。
proxy 只加入到 frontend网络。
db 只加入到backend网络。
app同时加入到 frontend和backend 。
db和proxy不能通讯，因为不在一个网络中。
app和两个都能通讯，因为app在两个网络中都有配置。
db和proxy要通讯，只能通过app这个应用来连接。

3.3.26 restart
no：是默认的重启策略，在任何情况下都不会重启容器。
always：容器总是重新启动。
on-failure：在容器非正常退出时（退出状态非0），才会重启容器。
unless-stopped：在容器退出时总是重启容器，但是不考虑在Docker守护进程启动时就已经停止了的容器
restart: "no"
restart: always
restart: on-failure
restart: unless-stopped
注：swarm 集群模式，请改用 restart_policy。
3.2.27 secrets存储敏感数据，例如密码：
version: "3.1"
services:

mysql:
  image: mysql
  environment:
    MYSQL_ROOT_PASSWORD_FILE: /run/secrets/my_secret
  secrets:
    - my_secret

secrets:
  my_secret:
    file: ./my_secret.txt
2.2.28 security_opt 修改容器默认的 schema 标签。
security-opt：
  - label:user:USER   # 设置容器的用户标签
  - label:role:ROLE   # 设置容器的角色标签
  - label:type:TYPE   # 设置容器的安全策略标签
  - label:level:LEVEL  # 设置容器的安全等级标签
2.2.29 stop_grace_period
指定在容器无法处理 SIGTERM (或者任何 stop_signal 的信号)，等待多久后发送 SIGKILL 信号关闭容器。
stop_grace_period: 1s # 等待 1 秒
stop_grace_period: 1m30s # 等待 1 分 30 秒
默认的等待时间是 10 秒。
3.2.30 stop_signal 设置停止容器的替代信号。默认情况下使用 SIGTERM。
以下示例，使用 SIGUSR1 替代信号 SIGTERM 来停止容器。

stop_signal: SIGUSR1
3.3.31 sysctls 设置容器中的内核参数，可以使用数组或字典格式。
sysctls:
  net.core.somaxconn: 1024
  net.ipv4.tcp_syncookies: 0
或
sysctls:
  - net.core.somaxconn=1024
  - net.ipv4.tcp_syncookies=0
2.3.32 tmpfs 在容器内安装一个临时文件系统。可以是单个值或列表的多个值。
tmpfs: /run
或
tmpfs:
  - /run
  - /tmp
3.3.33 ulimits 覆盖容器默认的 ulimit。
ulimits:
  nproc: 65535
  nofile:
    soft: 20000
    hard: 40000
3.3.34 volumes 将主机的数据卷或着文件挂载到容器里。用来存储docker持久化的数据，启动容器后，读取的是主机目录中的文件包
docker-compose里两种设置方式都是可以持久化的,绝对路径的和卷标的
创建数据卷：docker volume create testdir
查看数据卷信息：docker volume inspect testdir
查看全部数据卷：docker volume ls
删除数据卷：docker volume rm testdir
目录映射，可以直接使用[主机:容器]格式，或者使用[主机:容器:ro]格式，后者对于容器来说，数据卷是只读的，可以有效保护宿主机的文件系统
注意：容器目录不可以为相对路径，必须以下斜线“/”开头
宿主机目录如果不存在，则会自动生成，容器删除销毁不会导致宿主机相应目录的删除
version: "3.7"
services:
  db:
    image: postgres:latest
    volumes:
      - /var/lib/postgres #只指定一个路径，Docker会自动在创建一个目录
      - "/localhost/postgres.sock:/var/run/postgres/postgres.sock"
      - "/localhost/data:/var/lib/postgresql/data" #将主机的/localhost/data目录挂载到容器中/var/lib/postgresql/data目录
      - $PWD/:/test_pwd #绝对路径，表示将物理机当前目录映射到docker虚拟机/test_pwd里面
      - ./test1:/tmp/cache #相对路径，以Compose配置文件的目录为中心的映射，在/var/lib/docker/volumes/test1/_data（通过docker inspect命令，查看容器“Mounts”那一部分）
      - /test2 #只是-v指定一个目录，同上面类似，只不过它不是相对路径的目录名，而是随机生成的一个目录名/var/lib/docker/volumes/96256232eb74edb139d652746f0fe426e57fbacdf73376963e3acdb411b3d73a/_data
      - db:/var/lib/db #卷标的
    privileged: true #设置容器的权限为root
如：# docker run -it --privileged=true -v /test:/soft centos /bin/bash
修改docker容器的目录映射
方法1、删除原有容器，重新创建新的容器
方法2、修改容器配置文件
1.暂停Docker服务 systemctl stop docker
2.进入 Docker 容器配置文件目录下对应容器目录cd /var/lib/docker/containers/idxxx...
3.修改 config.v2.json和hostconfig.json
4.重新启动 Docker 服务
方法3、使用 commit 构建新镜像，先删了旧容器，再改名
3.3.35 privileged 用来给容器root权限，不安全的
挂载宿主机已存在目录后，在容器内对其进行操作，报“Permission denied”。
可通过两种方式解决：
1 关闭selinux。
临时关闭：# setenforce 0
永久关闭：修改/etc/sysconfig/selinux文件，将SELINUX的值设置为disabled。
2 以特权方式启动容器 
指定--privileged参数
3.3.36 external_links 链接到docker-compose.yml外部的容器
external_links：
  - redis_1
  - project_db_1:mysql
```


## 二、Kubernetes 入门&进阶实战
### 1.K8S概览
- Kubernetes（K8S）教程 https://k8s.easydoc.net/docs/dRiQjyTY/28366845/6GiNOzyZ/nd7yOvdY
### 1.1 K8S 是什么？
    用于自动部署、扩展和管理“容器化（containerized）应用程序”的开源系统。（K8S 是负责自动化运维管理多个Docker程序的集群）
### 1.2 K8S 做什么？
    自动化运维管理 Docker（容器化）程序。(自动完成服务的部署、更新、卸载和扩容、缩容),K8S 核心功能就是部署运维容器化服务。
### 1.3 K8S 怎么做？
    K8S 是属于主从设备模型（Master-Slave 架构），即主节点(Master Node)负责核心的调度、管理和运维，从节点(Worker Node)则在执行用户的程序。分别安装了 K8S 的 Master 和 Woker 组件的实体服务器，每个 Node 都对应了一台实体服务器，组成了 K8S 集群
#### 1.3.1 Master Node都有哪些组件：
- API Server。K8S 的请求入口服务：负责接收 K8S 所有请求（来自 UI 界面或者 CLI 命令行工具），然后，API Server 根据用户的具体请求，去通知其他组件干活。
- Scheduler。K8S 所有 Worker Node 的调度器：当用户要部署服务时，Scheduler 会选择最合适的 Worker Node（服务器）来部署。
- Controller Manager。K8S 所有 Worker Node 的监控器：负责监控和调整在 Worker Node 上部署的服务的状态，调度 Scheduler进行执行。Controller Manager 有很多具体的 如Node Controller、Service Controller、Volume Controller 等
- Etcd。K8S 的存储服务：etcd 存储了 K8S 的关键配置和用户配置，K8S 中仅 API Server 才具备读写权限，其他组件必须通过 API Server 的接口才能读写数据
#### 1.3.2 Worker Node都有哪些组件：
- Kubelet。Worker Node 的监视器，以及与 Master Node 的通讯器。Kubelet 是 Master Node 安插在 Worker Node 上的“眼线”，它会定期向 Worker Node 汇报自己 Node 上运行的服务的状态，并接受来自 Master Node 的指示采取调整措施。
- Kube-Proxy。K8S 的网络代理。Kube-Proxy 负责 Node 在 K8S 的网络通讯、以及对外部网络流量的负载均衡。
- Container Runtime。Worker Node 的运行环境。即安装了容器化所需的软件环境确保容器化程序能够跑起来，比如 Docker Engine。大白话就是帮忙装好了 Docker 运行环境。
- Logging Layer。K8S 的监控状态收集器。负责采集 Node 上所有服务的 CPU、内存、磁盘、网络等监控项信息。
- Add-Ons。K8S 管理运维 Worker Node 的插件组件。Add-On 机制，让用户可以扩展更多定制化功能。
> 总结：  
> K8S 的 Master Node 具备：请求入口管理（API Server），Worker Node 调度（Scheduler），监控和自动调节（Controller Manager），以及存储功能（etcd）；  
> K8S 的 Worker Node 具备：状态和监控收集（Kubelet），网络和负载均衡（Kube-Proxy）、保障容器化运行环境（Container Runtime）、以及定制化功能（Add-Ons）。

## 2.K8S 重要概念
### 2.1 Pod 实例
    Pod是可以在 Kubernetes 中创建和管理的、最小的可部署的计算单元。Pod 可以被理解成一群可以共享网络、存储和计算资源的容器化服务的集合,同一个 Pod 里的几个 Docker 服务/程序，好像被部署在同一台机器上，可以通过 localhost 互相访问，并且可以共用 Pod 里的存储资源。不同的 Pod 之间的 Container 不能用 localhost 访问，也不能挂载其他 Pod 的数据卷。
    K8S 集群内的每一个 Pod 都有自己的 IP（是不是很类似一个 Pod 就是一台服务器，然而事实上是多个 Pod 存在于一台服务器上，只不过是 K8S 做了网络隔离），在 K8S 集群内部还有 DNS 等网络服务（一个 K8S 集群就如同管理了多区域的服务器，可以做复杂的网络拓扑）。
```yaml memory-demo.yaml
apiVersion: v1
kind: Pod
metadata:
  name: memory-demo
  namespace: mem-example
spec:
  containers:
  - name: memory-demo-ctr
    image: polinux/stress
    resources:
      limits:
        memory: "200Mi"
      requests:
        memory: "100Mi"
    command: ["stress"]
    args: ["--vm", "1", "--vm-bytes", "150M", "--vm-hang", "1"]
    volumeMounts:
    - name: redis-storage
      mountPath: /data/redis
  volumes:
  - name: redis-storage
    emptyDir: {}
```
- apiVersion记录 K8S 的 API Server 版本，现在看到的都是v1，用户不用管。
- kind记录该 yaml 的对象，比如这是一份Pod的yaml配置文件，那么值内容就是Pod。
- metadata记录了 Pod 自身的元数据，比如name,这个 Pod 的名称。这个 Pod 属于哪个namespace（命名空间暂时理解为“同一个命名空间内的对象互相可见”）。
- spec记录了 Pod 内部所有的资源的详细信息
- containers记录了 Pod 内的容器信息，containers包括了：namePod 下该容器名称，image容器的镜像地址，resources容器需要的 CPU、内存、GPU 等资源，limits是 K8S 为该容器至多分配的资源配额；而requests则是 K8S 为该容器至少分配的资源配额。command容器的入口命令，args容器的入口参数，volumeMounts容器要挂载的 Pod 数据卷等。可以看到，上述这些信息都是启动容器的必要和必需的信息。
- volumes记录了 Pod 内的数据卷信息。

### 2.2 Volume 数据卷
    数据卷 volume 是 Pod 内部的磁盘资源。K8S 支持很多类型的 volume 数据卷挂载。volume 是 K8S 的对象，对应一个实体的数据卷；而 volumeMounts 只是 container 的挂载点，对应 container 的其中一个参数。但是，volumeMounts 依赖于 volume，只有当 Pod 内有 volume 资源的时候，该 Pod 内部的 container 才可能有 volumeMounts。
### 2.3 Container 容器
    一个 Pod 内可以有多个容器 container。容器分类：标准容器 Application Container，初始化容器 Init Container，边车容器 Sidecar Container，临时容器 Ephemeral Container。
### 2.4 Deployment 和 ReplicaSet（简称 RS）
    Deployment 的作用是管理和控制 Pod 和 ReplicaSet，管控它们运行在用户期望的状态中。    
    ReplicaSet 的作用就是管理和控制 Pod，管控他们好好干活。但是，ReplicaSet 受控于 Deployment。形象来说，ReplicaSet 就是总包工头手下的小包工头。
### 2.5 Service 和 Ingress
    负责管控 Pod 网络服务。
    K8S 中的服务（Service）并不是我们常说的“服务”的含义，而更像是网关层，是若干个 Pod 的流量入口、流量均衡器。Service 主要负责 K8S 集群内部的网络拓扑。集群外部访问集群内部则需要Ingress。
    Service 是 K8S 服务的核心，屏蔽了服务细节，统一对外暴露服务接口，真正做到了“微服务”。举个例子，我们的一个服务 A，部署了 3 个备份，也就是 3 个 Pod；对于用户来说，只需要关注一个 Service 的入口就可以，而不需要操心究竟应该请求哪一个 Pod。优势非常明显：一方面外部用户不需要感知因为 Pod 上服务的意外崩溃、K8S 重新拉起 Pod 而造成的 IP 变更，外部用户也不需要感知因升级、变更服务带来的 Pod 替换而造成的 IP 变化，另一方面，Service 还可以做流量负载均衡。
    Ingress 是整个 K8S 集群的接入层，负责集群内外通讯。
### 2.6 namespace 命名空间
    Kubernetes 支持多个虚拟集群，它们底层依赖于同一个物理集群。 这些虚拟集群被称为命名空间。可以通过在 K8S 集群内创建 namespace 来分隔资源和对象。
    # 位于命名空间中的资源kubectl api-resources --namespaced=true
    # 不在命名空间中的资源kubectl api-resources --namespaced=false

## 3.配置 kubectl
### 3.1 Kubectl
    Kubectl 是一个命令行接口，用于对 Kubernetes 集群运行命令。Kubectl 的配置文件在$HOME/.kube 目录。我们可以通过设置 KUBECONFIG 环境变量或设置命令参数--kubeconfig 来指定其他位置的 kubeconfig 文件。
    基本语法：kubectl [command] [TYPE] [NAME] [flags]
- command：指定要对一个或多个资源执行的操作，例如 create、get、describe、delete。
- TYPE：指定资源类型。资源类型不区分大小写，可以指定单数、复数或缩写形式。
- NAME：指定资源的名称。名称区分大小写。如果省略名称，则显示所有资源的详细信息
- flags: 指定可选的参数。例如，可以使用 `-s` 或 `-server` 参数指定 Kubernetes API 服务器的地址和端口。
> 要按类型和名称指定资源：`YPE1 name1 name2 name<#>`,例kubectl get pod example-pod1 example-pod2
> 分别指定多个资源类型：`TYPE1/name1 TYPE1/name2 TYPE2/name3 TYPE<#>/name<#>`
例kubectl get pod/example-pod1 replicationcontroller/example-rc1
> 用一个或多个文件指定资源：`-f file1 -f file2 -f file<#>`例kubectl get -f ./pod.yaml

> 注意：kubectl 是 K8S 的命令行工具，并不需要 kubectl 安装在 K8S 集群的任何 Node 上，但是，需要确保安装 kubectl 的机器和 K8S 的集群能够进行网络互通。
### 3.2 配置Kubectl
#### 3.2.1 第一步，必须准备好要连接/使用的 K8S 的配置文件
```yaml
apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: thisisfakecertifcateauthoritydata00000000000
    server: https://1.2.3.4:1234
  name: cls-dev
contexts:
- context:
    cluster: cls-dev
    user: kubernetes-admin
  name: kubernetes-admin@test
current-context: kubernetes-admin@test
kind: Config
preferences: {}
users:
- name: kubernetes-admin
  user:
    token: thisisfaketoken00000
```
    解读如下：
- clusters记录了 clusters（一个或多个 K8S 集群）信息：
  - name是这个 cluster（K8S 集群）的名称代号
  - server是这个 cluster（K8S 集群）的访问方式，一般为 IP+PORT
  - certificate-authority-data是证书数据，只有当 cluster（K8S 集群）的连接方式是 https 时，为了安全起见需要证书数据
- users记录了访问 cluster（K8S 集群）的账号信息：
  - name是用户账号的名称代号
  - user/token是用户的 token 认证方式，token 不是用户认证的唯一方式，其他还有账号+密码等。
- contexts是上下文信息，包括了 cluster（K8S 集群）和访问 cluster（K8S 集群）的用户账号等信息：
  - name是这个上下文的名称代号
  - cluster是 cluster（K8S 集群）的名称代号
  - user是访问 cluster（K8S 集群）的用户账号代号
- current-context记录当前 kubectl 默认使用的上下文信息
- kind和apiVersion都是固定值，用户不需要关心
- preferences则是配置文件的其他设置信息，笔者没有使用过，暂时不提。
#### 3.2.2 第二步，给 kubectl 配置上配置文件。
- --kubeconfig参数。第一种办法是每次执行 kubectl 的时候，都带上`--kubeconfig=${CONFIG_PATH}`。给一点温馨小提示：每次都带这么一长串的字符非常麻烦，可以用 alias 别名来简化码字量，比如alias -k=kubectl --kubeconfig=${CONFIG_PATH}。
- KUBECONFIG环境变量。第二种做法是使用环境变量KUBECONFIG把所有配置文件都记录下来，即`export KUBECONFIG=$KUBECONFIG:${CONFIG_PATH}`。接下来就可以放心执行 kubectl 命令了。
- $HOME/.kube/config 配置文件。第三种做法是把配置文件的内容放到$HOME/.kube/config 内。具体做法为：
如果`$HOME/.kube/config` 不存在，那么`cp ${CONFIG_PATH} $HOME/.kube/config`即可；
如果已经存在，那么需要把新的配置内容加到HOME/.kube/config 下。单单只是`cat ${CONFIG_PATH} >> $HOME/.kube/config`是不行的，正确的做法是：`KUBECONFIG=$HOME/.kube/config:${CONFIG_PATH} kubectl config view --flatten > $HOME/.kube/config`。解释下这个命令的意思：先把所有的配置文件添加到环境变量KUBECONFIG中，然后执行`kubectl config view --flatten`打印出有效的配置文件内容，最后覆盖`$HOME/.kube/config` 即可。

> 请注意，上述操作的优先级分别是 1>2>3，也就是说，kubectl 会优先检查--kubeconfig，若无则检查KUBECONFIG，若无则最后检查$HOME/.kube/config，如果还是没有，报错。但凡某一步找到了有效的 cluster，就中断检查，去连接 K8S 集群了。
#### 3.2.3 第三步：配置正确的上下文
- kubectl config get-contexts。列出所有上下文信息。
- kubectl config current-context。查看当前的上下文信息。
- kubectl config use-context ${CONTEXT_NAME}。更改上下文信息。
- `kubectl config set-context ${CONTEXT_NAME}|--current --${KEY}=${VALUE}`。修改上下文的元素。比如可以修改用户账号、集群信息、连接到 K8S 后所在的 namespace。
- 上下文信息所包括的内容有：cluster 集群（名称）、用户账号（名称）、连接到 K8S 后所在的 namespace，因此有config set-context严格意义上的用法：`
kubectl config set-context [NAME|--current] [--cluster=cluster_nickname] [--user=user_nickname] [--namespace=namespace] [options]`
（备注：[options]可以通过 kubectl options 查看）

### 3.3 kubectl部署服务
#### 3.3.1 如何部署 Pod？
    通过 kubectl 部署 Pod 的办法分为两步：1. 准备 Pod 的 yaml 文件；2. 执行 kubectl 命令部署
- 第一步：准备 Pod 的 yaml 文件。如1113行memory-demo.yaml文件
- 第二步：执行 kubectl 命令部署。有了 Pod 的 yaml 文件之后，就可以用 kubectl 部署了，命令非常简单：kubectl create -f ${POD_YAML}。
#### 3.3.2 如何部署 Deployment？
##### 3.3.2.1第一步：准备 Deployment 的 yaml 文件。
```yaml Deployment.yaml
apiVersion: extensions/v1beta1
 kind: Deployment
 metadata:
   name: rss-site
   namespace: mem-example
 spec:
   replicas: 2
   template:
     metadata:
       labels:
         app: web
     spec:
      containers:
       - name: memory-demo-ctr
         image: polinux/stress
         resources:
         limits:
           emory: "200Mi"
         requests:
           memory: "100Mi"
         command: ["stress"]
         args: ["--vm", "1", "--vm-bytes", "150M", "--vm-hang", "1"]
         volumeMounts:
         - name: redis-storage
           mountPath: /data/redis
     volumes:
     - name: redis-storage
       emptyDir: {}
```
- metadata同 Pod 的 yaml，这里提一点：如果没有指明 namespace，那么就是用 kubectl 默认的 namespace（如果 kubectl 配置文件中没有指明 namespace，那么就是 default 空间）。
- spec，可以看到 Deployment 的spec字段是在 Pod 的spec内容外“包了一层”，那就来看 Deployment 有哪些需要注意的：
  - replicas。副本个数。也就是该 Deployment 需要起多少个相同的 Pod，如果用户成功在 K8S 中配置了 n（n>1）个，那么 Deployment 会确保在集群中始终有 n 个服务在运行。
  - template。
    - metadata
    - spec，会发现这完完全全是上文提到的 Pod 的spec内容，在这里写明了 Deployment 下属管理的每个 Pod 的具体内容。
##### 3.3.2.2第二步：执行 kubectl 命令部署。
    Deployment 的部署办法同 Pod：kubectl create -f ${DEPLOYMENT_YAML}。 (K8S 会根据配置文件中的kind字段来判断具体要创建的是什么资源。)
    部署完 deployment 之后，可以查看到自动创建了 ReplicaSet 和 Pod。k get deployment,k get rs, k get pod
### 3.4 kubectl 查看、更新/编辑、删除服务
#### 3.4.1如何查看服务？
    在 K8S 中，一个独立的服务即对应一个 Pod。即，当我们说要 xxx 一个服务的就是，也就是操作一个 Pod。而与 Pod 服务相关的且需要用户关心的，有 Deployment。
- 通过 kubectl 查看服务的基本命令是：`kubectl get|describe ${RESOURCE} [-o ${FORMAT}] -n=${NAMESPACE}`，${RESOURCE}有: pod、deployment、replicaset(rs)。
- 查看集群中所有的 namespace？`kubectl get ns`,`kubectl get pod --all-namespaces`
通过-n=${NAMESPACE}就可以指定自己要操作的资源所在的 namespace,比如查看 Pod：kubectl get pod -n=oona-test，同理，查看 Deployment：kubectl get deployment -n=oona-test。
- 查找所有的命名空间下的 Deployment 的命令是：kubectl get deployment --all-namespaces。
#### 3.4.2 如何更新/编辑服务？
    两种办法：1. 修改 yaml 文件后通过 kubectl 更新；2. 通过 kubectl 直接编辑 K8S 上的服务。
- 方法一：通过 kubectl 更新的命令是`kubectl apply -f ${YAML}` (也可以用于首次创建一个服务)
- 方法二：通过 kubectl 直接编辑 K8S 上的服务。命令为`kubectl edit ${RESOURCE} ${NAME}`
#### 3.4.3 如何删除服务？
- `kubectl delete ${RESOURCE} ${NAME}`。比如删除一个 Pod 是：`kubectl delete pod memory-demo`，再比如删除一个 Deployment 的命令是：`kubectl delete deployment ${DEPLOYMENT_NAME}`
> 如果只部署了一个 Pod，那么直接删除该 Pod 即可,如果是通过 Deployment 部署的服务，那么仅仅删除 Pod 是不行的，正确的删除方式应该是：先删除 Deployment，再删除 Pod。仅仅删除了 Pod 但是 Deployment 还在的话，Deployment 定时会检查其下属的所有 Pod，如果发现失败了则会再拉起。
- 强制删除措施，命令为`kubectl delete pod --force --grace-period=0 ${POD_NAME}`。
### 3.5 kubectl 排查服务问题
#### 3.5.1K8S 上部署服务失败了怎么排查？
- 命令：`kubectl describe ${RESOURCE} ${NAME}`
一般来说，通过kubectl describe pod ${POD_NAME}已经能定位绝大部分部署失败的问题了

#### 3.5.2K8S 上部署的服务不正常怎么排查
    如果服务部署成功了，且状态为running，那么就需要进入 Pod 内部的容器去查看自己的服务日志了：
- 查看Pod内部某个container 打印的日志：`kubectl log ${POD_NAME} -c ${CONTAINER_NAME}`。
- 进入Pod内部某个container：`kubectl exec -it [options] ${POD_NAME} -c ${CONTAINER_NAME} [args]`，嗯，这个命令的作用是通过 kubectl 执行了docker exec xxx进入到容器实例内部。之后，就是用户检查自己服务的日志来定位问题。

### 3.6安装minikube  
    minikube 的官网上提供了各种系统的安装命令，通常就是下载、拷贝这两步，不过你需要注意一下本机电脑的硬件架构，Intel 芯片要选择带“amd64”后缀，Apple M1 芯片要选择“arm64”后缀，选错了就会因为 CPU 指令集不同而无法运行。
    官方地址https://minikube.sigs.k8s.io/docs/start/
    网速实在太慢了，推荐使用阿里云的镜像来进行安装，阿里云发布的minikube地址：https://github.com/AliyunContainerService/minikube
#### 3.6.1 直接安装minikube
    curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && mv minikube /usr/local/bin/
#### 3.6.2 启动minikube
    1.默认会使用docker容器。从 Docker Hub 上拉取镜像，以当前最新版本的 Kubernetes 启动集群，可以在后面再加上一个参数 --kubernetes-version，明确指定要使用 Kubernetes 版本。
    minikube start --registry-mirror=https://registry.docker-cn.com --force --driver=docker --kubernetes-version=v1.26.3
    minikube version查看版本号
    2. 如果安装失败，请先删除后再重新安装:minikube delete --all --purge
    3. 如果出现拉取镜像失败的情况，可以先尝试安装好对应的镜像文件,然后 minikube 在启动的时候使用本地的镜像，这样可以减少 minikube start 过程的耗时
    minikube start --vm-driver=docker --base-image="bitnami/etcd:3"
    4. 停止集群 minikube stop
    5. 清空集群 minikube delete --all
```shell
常用配置参数如下
--driver=*** 从1.5.0版本开始，Minikube缺省使用系统优选的驱动来创建Kubernetes本地环境，比如您已经安装过Docker环境，minikube 将使用 docker 驱动
--cpus=2: 为minikube虚拟机分配CPU核数
--memory=2048mb: 为minikube虚拟机分配内存数
--registry-mirror=*** 为了提升拉取Docker Hub镜像的稳定性，可以为 Docker daemon 配置镜像加速,和启动的 minikube 内部的 docker.daemon 文件中所指向的镜像仓库地址一致
--kubernetes-version=***: minikube 虚拟机将使用的 kubernetes 版本
--base-image 声明好基础镜像，如果宿主机内部有对应镜像，就不需要额外拉取
--image-repository 拉取镜像的仓库
--kubernetes-version 指定 kubernetes 版本
--force 如果使用 root 账号，需要加上此参数
比如， 创建 minikube 环境并且调整默认资源配置
minikube start \
--kubernetes-version=v1.26.3
--registry-mirror=https://bmtb464.mirror.aliyuncs.com \
--driver=docker \
--base-image="bitnami/etcd:3.5.8" \
--image-repository-registry.cn-hangzhou.aliyuncs.com/google_containers \
--image-mirror-country='cn' \
--cpus=4 \
--memory=4096mb \
--force
```
#### 3.6.3 安装kubectl客户端命令工具
    1. kubectl是集群命令行交互工具,与 Kubernetes 后台服务通信，把我们的命令转发给 Kubernetes，实现容器和集群的管理功能。minikube 管理 Kubernetes 集群环境，kubectl 操作实际的 Kubernetes 功能。
    minikube kubectl -- get po -A
    2. 此时的minikube kubectl --就相当于k8s里的kubectl命令，当然我们实际不会这样使用，我们可以使用 Linux 的alias功能，为它创建一个别名，写到当前用户目录下的 .bashrc 里：
    alias kubectl="minikube kubectl --"
    3. 此时再直接运行kubectl命令：kubectl version --short
    4. 查看集群信息kubectl cluster-info
    5. 查看节点kubectl get node -A
    6. 查看内部服务组件kubectl get pod -A

#### 3.6.4 开启控制台
    安装集群可视化Web UI控制台minikube dashboard
    直接点击生成的url，即可看到控制台页面(正常启动过的情况下，dashboard 默认会以本地回环地址拉起proxy)
    主机访问虚拟机上的dashboard
```shell
kubectl proxy --port=42770 --address='0.0.0.0' --disable-filter=true --accept-hosts='^.*' 
或者
kubectl proxy --port=42770 --address='192.168.1.35' --accept-hosts='^.*'
# kube-proxy 网络代理，负责网络相关的工作
# 42770：是指定的一个端口，没有使用的
# 192.168.1.35：虚拟机的主机ip
```
```shell
一些常见问题
1.执行minikube start出现 The "docker" driver should not be used with root privileges 的报错.
如果是本地测试环境，根本就不需要考虑那么多，直接执行以下命令，强制使用docker：
minikube start --force --driver=docker
# 或者使用阿里云镜像启动
minikube start --force --driver=docker --image-mirror-country cn --iso-url=https://kubernetes.oss-cn-hangzhou.aliyuncs.com/minikube/iso/minikube-v1.5.0.iso --registry-mirror=https://xxxxxx.mirror.aliyuncs.com 

2.执行istioctl install命令时一直出现如下问题：
failed to wait for resource: resources not ready after 5m0s: timed out waiting for the condition
此时使用kubectl get pods -n istio-system命令发现istio-egressgateway和istio-ingressgateway都处于ContainerCreateing状态。
解决方式：等了很久（10分钟左右），自动就好了。原因暂时未知，google说可能是node的问题。
```
### 3.6.5 使用阿里云代理http://k8s.gcr.io镜像仓库
    1. 国内根本访问不了k8s的镜像库：k8s.gsc.io,这时候去指定国内的阿里云镜像代理仓库进行下载
    docker pull registry.aliyuncs.com/google_containers/coredns:1.6.5
    2. 然后打tag，并删除之前从代理仓库下载的镜像
    docker tag registry.aliyuncs.com/google_containers/coredns:1.6.5 k8s.gcr.io/coredns:1.6.5
    docker rmi registry.aliyuncs.com/google_containers/coredns:1.6.5
> 注意:
确定imagePullPolicy镜像下载策略是IfNotPresent，即本地有镜像则使用本地镜像，不拉取！
或者将下载好的镜像放到harbor私有仓库里，然后将image下载地址指向harbor仓库地址。

### 3.6.6 Minikube 基础操作
- 1、基础命令行  
启动并运行一个集群：minikube start  
访问 minikube中的 k8s dashboard：minikube dashboard  
创建一个服务：kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4  
以 NodePort 的形式暴露一个服务：kubectl expose deployment hello-minikube --type=NodePort --port=8080  
使用minikube在浏览器中快速打开服务放出的endpoint：minikube service hello-minikube  
升级集群：minikube start --kubernetes-version=latest  
启动另一个本地集群：minikube start -p cluster2  
停止一个集群：minikube stop  
删除一个集群：minikube delete  
删除本地所有集群和配置：minikube delete --all  
- 2、发布应用  
  - 1）通过 kubectl 发布服务  
  1. 创建服务:：kubectl create deployment hello-minikube1 --image=registry.cn-hangzhou.aliyuncs.com/google_containers/echoserver:1.10
  2. 暴露端口:kubectl expose deployment hello-minikube1 --type=LoadBalancer --port=8080
  3. 查看映射端口:export PORT=$(kubectl get svc hello-minikube1 -o go-template='{{range.spec.ports}}{{if .nodePort}}{{.nodePort}}{{"\n"}}{{end}}{{end}}')  
  查看端口echo $PORT  
  4. 访问端口:minikube service hello-minikube1  
  5. 删除服务:kubectl delete deployment -n default hello-minikube1 --force --grace-period=0  
  kubectl delete service hello-minikube1  
  - 2）通过 Addons 管理插件  
    Minikube 自带了一个内置应用列表，包括诸如 Istio、Ingress 等，可以方便快速部署插件。  
  1. 查询插件列表:minikube addons list  
  2. 启用指定插件:minikube addons enable <name>  
  3. 同时启用多个插件:minikube start --addons <name1> --addons <name2>  
  4. 在浏览器打开插件暴露出的endpoint:minikube addons open <name>  
  5. 停用指定插件:minikube addons disable <name>  
- 3、访问应用  
  - 1）NodePort 方式访问  
    NodePort 方式是访问服务最基础的方式，顾名思义，就是将端口映射到本地，并通过本地的 IP + 映射的端口访问服务放出的 endpoint，这种方式下，服务会共用 VM 的 IP。  
  1. 使用service命令访问endpoint:minikube service --url <service-name>  
  2. 使用 kubectl获取nodePort 端口,通过minikube ip 命令可以获取到虚拟机的IP地址，执行以下命令，可以获取到服务映射的 nodePort 端口:  
  kubectl get service <service-name> --output='jsonpath="{.spec.ports[0].nodePort}"'  
  3. 扩展 NodePort 的范围,一般来说，minikube 包括的端口范围为 30000-32767，如果不够的话，可以通过如下命令进行扩展:  
  minikube start --extra-config=apiserver.service-node-port-range=1-65535
  - 2）LoadBalancer 方式访问  
    LoadBalancer 方式，是将服务暴露到公网中的标准方法，使用这种方法，每一个服务都有其独立的IP。

    以 LoadBalancer 方式暴露的服务需要通过 minikube tunnel 命令访问，并且必须在一个独立的终端窗口保持 LoadBalancer 运行，使用 Ctrl-C 可以退出进程，但是相关的路由信息将会被情况
  1. 使用 minikube tunnel:minikube tunnel  
  在独立的终端运行 tunnel，它会在k8s的CIDR中新增路由规则，将集群的IP地址作为网关，tunnel 命令会将服务的外部访问IP直接暴露给主机操作系统上运行的所有程序。  
  2. 创建一个deployment:kubectl create deployment hello-minikube1 --image=registry.cn-hangzhou.aliyuncs.com/google_containers/echoserver:1.10  
  检查服务:kubectl get pod  
  3. 创建LB服务，将服务暴露出来:kubectl expose deployment hello-minikube1 --type=LoadBalancer --port=8080  
  4. 查看外部访问IP:kubectl get svc  
  5. 在浏览器中访问服务（通过IP:Port）:打开浏览器，访问http://127.0.0.1:8080，（确保服务没有proxy设置）

- 4、Minikube Dashboard
  - 1）基础使用minikube dashboard,这将会开启 dashboard 插件，，并自动在默认浏览器中开启代理的 endpoint，同样，这也需要在终端中保持进程运行，使用Ctrl + C 结束代理，之后 dashboard 将不能使用。
  - 2）获取 dashboard 的URL,如果你不想直接在浏览器中打开代理，也可以执行以下命令，这会只返回可访问的URL地址：minikube dashboard --url
### 3.5 K8S基本使用
#### 3.5.1 创建Namespace  
（1）使用命令行方式创建kubectl create namespace testmk01  
（2）使用yaml文件创建
创建一个名为testmk02-ns.yaml的yaml文件
```yaml
apiVersion: v1
kind: Namespace
metadata:
  name: testmk02
```
然后使用如下命令进行创建
kubectl create -f testmk02-ns.yaml或kubectl apply -f testmk02-ns.yaml
查看Namespace:kubectl get ns 或者 kubectl get namespace  
#### 3.5.2创建Pod
1、创建一个名为test_pod1.yaml的yaml
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: pod-test1
  namespace: testmk01   #指定命名空间
  labels:
    name: pod-test1
spec:
  containers:
  - name: pod-test1
    image: nginx:latest
    imagePullPolicy: IfNotPresent
    ports:
    - containerPort: 80
```
然后使用如下命令创建： kubectl create -f test_pod1.yaml  
2、查看Pod  
kubectl get pods  
kubectl get pods --namespace testmk01  
kubectl get pods -A  
kubectl get pods/pod-test1 -o=wide -n testmk01  
#### 3.5.3执行容器命令
（1）执行pod的某个命令，默认使用pod的第一个容器执行  
kubectl exec pod-test1 ls -n testmk01  
（2）指定pod的某个容器执行命令
kubectl exec <pod-name> -c <container-name> date  
（3）进入容器  
kubectl exec -it <pod-name> -c <container-name> /bin/bash  
kubectl exec -it pod-test1 /bin/bash -n testmk01  
#### 3.5.4创建Replication Controller
（1）使用命令方式创建Deployment控制器 
1、创建控制器 
kubectl run nginx --image=nginx:latest --imagePullPolicy=IfNotPresent --replicas=3  
（2）使用yaml文件创建ReplicationController  
创建一个nginx.yaml文件
```yaml
apiVersion: v1
kind: ReplicationController
metadata:
  name: nginx
  labels:
    name: nginx
spec:
  replicas: 1
  selector:
    name: nginx
  template:
    metadata:
      name: nginx
      labels:
        name: nginx
    spec:
      containers:
      - name: nginx
        image: nginx
        imagePullPolicy: IfNotPresent
        ports:
        - containerPort: 80
```
然后使用如下命令创建： kubectl create -f nginx.yaml  
2、查看控制器  
如果是查看Deployment控制器kubectl get deployment  
如果是查看Replication Controller  
kubectl get rc或kubectl get replicationcontroller  
如果有设置命名空间，需要在后面加上-n参数或者--namespace指定Namespace  
#### 3.5.5 Service增删查1、创建Service
（1）使用命令行创建  
kubectl expose rc rc-name --type=ClusterIP --target-port=80 --port=80  
（2）使用yaml文件创建  
创建一个nginx-service.yam文件  
```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx
  labels:
    name: nginx
spec:
  type: NodePort
  ports:
  - port: 80
    nodePort: 30002
  selector:
    name: nginx
```
然后使用如下命令创建：kubectl create -f nginx-service.yaml
查看 kubectl get svc 或 ubectl get service
如果指定了命名空间，则需要加上-n或--namespace参数指定Namespace

#### 3.5.6通用
1、查看某个资源的详细信息  
kubectl describe 资源类型 资源名称 或 ubectl describe 资源类型/资源名称  
kubectl describe pods/pod-test1 -n testmk01  
2、查看某个资源的日志  
kubectl logs 资源类型 资源名称 或 ubectl logs 资源类型/资源名称  
kubectl logs pods/pod-test1 -n testmk01  
跟踪查看容器的日志，相当于tail -f命令  
kubectl logs -f <pod-name> -c <container-name>  
3、删除拥有某个Label的资源  
kubectl delete 资源类型 -l name=<label-name>  

