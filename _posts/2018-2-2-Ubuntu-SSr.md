---
layout: post
title:  "Ubuntu 安装 ShodowSocksR"
date:   2018-2-2 21:32:18
categories: Ubuntu
tags: Ubuntu
excerpt: 记录梯子的搭建过程。
mathjax: true
---
##### Ubuntu 安装 ShodowSocksR

######  下载ShodowSocksR

	
  
	wget  https://github.com/shadowsocksr-backup/shadowsocksr/archive/3.1.2.zip
	tar xcf shadowsocksr-3.1.2.zip
	cd shadowsocksr-3.1.2
	

###### 快速配置

使用 shadowsocksr-3.1.2 只需要配置 `config.json` 文件即可。具体参数如下：


		{
    "server": "", //服务器地址
    "server_ipv6": "::",
    "server_port": 8080, 	// 服务器端口
    "local_address": "127.0.0.1", //
    "local_port": 1080,           //本地代理端口

    "password": "password",  //你的密码
    "method": "AES-256-CFB",//加密方式
    "protocol": "auth_sha1_v4", // 协议插件
    "protocol_param": "",
    "obfs": "tls1.2_ticket_auth",  //混淆插件
    "obfs_param": "",
    "speed_limit_per_con": 0,
    "speed_limit_per_user": 0,

    "additional_ports" : {}, // only works under multi-user mode
    "additional_ports_only" : false, // only works under multi-user mode
    "timeout": 120,
    "udp_timeout": 60,
    "dns_ipv6": false,
    "connect_verbose_info": 0,
    "redirect": "",
    "fast_open": false
	}


根据需要更改即可。
	
*附件免费的SS帐号：


    https://github.com/Alvin9999/new-pac/wiki/ss%E5%85%8D%E8%B4%B9%E8%B4%A6%E5%8F%B7


###### 运行

	
	python ./shadowsocks/local.py -c config.json
	



#####  本文仅仅记录shadowsocksr的使用，你还需要配置浏览器的插件。



