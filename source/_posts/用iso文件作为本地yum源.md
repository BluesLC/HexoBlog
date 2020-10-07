---
title: '用iso文件作为本地yum源'
url: 用iso文件作为本地yum源.html
categories:
  - Linux
date: 2019-02-27 23:53:11
tags:
  - Linux
---

## 一．挂载iso文件
`#mount -o loop /mnt/centos.dvd1.iso /mnt/cdrom0`
`#mount -o loop /mnt/centos.dvd2.iso /mnt/cdrom1`

## 二．将两个iso的package文件夹合并到一个文件夹
这一步可用命令行完成，此处用图形界面讲解

创建文件夹iso
`#mkdir iso`

将cdrom0 cdrom1两个文件夹内容拷贝至iso文件夹
![](/images/yum1.png)
拷贝覆盖中途会弹窗询问是否合并文件夹，选择Merge All
![](/images/yum2.png)

拷贝覆盖中途会弹窗询问是否替换文件，选择Skip All
## 三．配置yum源
切换至/etc/yum.repo.d/
`#cd  /etc/yum.repo.d/`

创建一个新的.repo文件
`#vim  rhel-dvd.repo`

添加内容
```
[dvd]
name=rhel_dvd
baseurl=file:///mnt/iso/
enabled=1
gpgcheck=0
```

保存
:wq

检验yum源是否可用
`#yum list openssl`