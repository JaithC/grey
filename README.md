# grey
grey批量部署工具

使用前需要先安装docker

# 安装

1、 wget https://github.com/greylinlin/grey/releases/download/0.0.4/gTool

2、 mv gTool /usr/bin

3、 chmod +x /usr/bin/gTool

#### 验证是否安装成功

gTool version
- 0.0.4
- 出现版本信息即为安装成功

# 使用
1、查看所有功能
 gTool -h
- address     获取已部署节点的地址
- completion  generate the autocompletion script for the specified shell
- deploy      gTool 部署命令
- help        Help about any command
- key         获取已部署节点的私钥
- restart     重启已部署完的节点
- transfer    批量注水
- version     打印gTool版本号

2、批量部署  
gTool deploy -s 1 -e 50  
即可部署50个节点

查看参数说明
gTool deploy -h

Usage:
gTool deploy [flags]

Flags:  
-e, --end int     使用 -e 设置结束 (default 20)  
-h, --help        help for deploy  
-s, --start int   使用 -s 设置起始 (default 1)


-s 代表节点开始数   -e代表节点结束

3、查看所有部署的节点地址  
gTool address -s 1 -e 50  
会在终端打印1-50节点的地址 并会在当前路径下生成address.txt

4、批量注水  
gTool transfer -p ./address.txt

-p代表需要注水的地址（address.txt一行一个地址，可以直接拿第三步的文件）

5、批量重启
gTool restart  -s 1 -e 50  
-s -e参数如上

6、获取私钥  
gTool key  -s 1 -e 50

7、余额查询  
gTool balance  -s 1 -e 50






