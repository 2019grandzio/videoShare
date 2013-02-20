#OpenWan媒体资产管理系统
=========

##为什么要引入媒体资产管理系统

媒体产业不断发展，第四代媒体已逐渐崛起，数字多媒体的应用，广播频道的扩充，媒体资源的多样性应用（一个节目被多种形式媒体采用）和重复使用（许多节目或素材被重新编辑后产生新的价值）显示出了它巨大的潜藏价值。而目前影视录像带、唱片等媒体资料的审看或回放是通过从大量无序的录像带和光盘中查找、调用，再通过录像机播放的方式操作，效率非常低，而且共享性能差，已经不能适应数字化时代的发展需要。同时，随着岁月的流逝，许多珍贵的历史资料和素材都急需加以复制和保护，由于磁带或唱片等介质存放保质期有限，而数量还在源源不断的增加，因此急需对其进行整理、复制和保存。 

媒体资产数字化、信息化、网络化、智能化的改造是当前音像资料管理发展的趋势。很多单位都保存了一大批具有历史意义和科研价值的视音频节目素材，庞大的视音频资料保存、管理和应用的难度很大，如何实现对这些媒体资料的有效管理，已成为所有单位面临的一个重要课题。 

为了长期保存珍藏的原始影像资料，为了快速检索所需要的影像资源，为了方便管理并具有高保密性和安全性，为了实现网上共享、浏览、播放，主要解决视音频等多媒体数据资料的数字化存储、编目管理、检索查询和资料发布等问题的媒体资产管理（Media Asset Management）系统将成为信息数字化过程中不可或缺的部分。

##OpenWan 概述

OpenWan媒体资产管理系统是以智能存储为中心，建立具有资源共享的数据化、网络化、自动化系统，能够支持广播电台、电视台各频道节目的数字化采集、编辑、播出、审查和存储等业务，为视频资料的利用与再利用提供简便、安全、快捷、准确可行的方法。 

OpenWan媒媒体资产管理系统集成了先进的硬件架构，采用MPEG-2、MPEG-4编码压缩技术，并融合数字视频压缩、网络传输、资料检索、存储管理、多媒体、数据库、WEB等技术，形成了一套集媒体资料创建、编目、存储、管理、检索和发布应用为一体的资产管理系统。

系统使用PHP语言开发，框架采用QeePHP2.1优秀的开发框架，Mysql数据库，媒体文件转码使用FFmpeg组件，全文检索使用Sphinx引擎，在线播放音乐及视频等。优秀的权限访问控制功能，包含：用户管理、用户组管理、角色管理、权限管理、浏览等级管理等。

1. 使用BSD开源协议，源代码完全开源，没有商业限制。
2. 使用PHP语言开发，简单易学，学习成本低，维护成本低。
3. 完全兼容目前最流行浏览器（IE6、IE7+、Firefox、Chrome）。

## 快速安装

1. 将程序拷贝到服务器站点目录下
2. 将 db/openwan_db_20100809.sql 导入到MySql数据库
3. 修改 config/database.yaml 数据库配置
4. 修改PHP配置（php.ini）
   post_max_size = 100M
   upload_max_filesize = 100M
   max_execution_time = 6000
5. 全文搜索引擎配置 （CSFT: coreseek.cn）
   运行csft\install.bat文件，安装搜索引擎
6. 启动Web浏览器，在地址栏中输入 http://localhost 按Enter键，即可进入OpenWan主页（用户名：admin 密码：admin）。

## 环境要求

操作系统: Windows NT 5.0 以上
服务器：Apache2或IIS5 + PHP5 以上
数据库：MySql 5.1 以上

## 常见问题

问题：如果你使用IIS服务器并无法进行视频转码。
解决：为C:\Windows\System32\cmd.exe（系统不是安装在C盘请相应更改）添加IUSER_ComputerName （ComputerName是你的计算机名称）允许用户的读取、运行权限。

## 更多文档

[OpenWan介绍演示.docx](https://github.com/thinkgem/openwan/raw/master/OpenWan%E4%BB%8B%E7%BB%8D%E6%BC%94%E7%A4%BA.docx)