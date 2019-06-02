
## 介绍 ##

一个Shell脚本，集成SSR多用户管理，流量限制，加密更改等基本操作。是一个基于ShadowsocksR官方的mujson的辅助脚本。方便用户操作，并且支持快速构建SSR服务环境。

## 系统支持 ##
* Ubuntu 14
* Ubuntu 16
* Debian 7
* Debian 8
* CentOS 6
* CentOS 7

## 功能 ##
- 全自动无人值守安装，服务端部署只需一条命令，您和SSR都是如此的优雅：）
- 一键开启、关闭SSR服务
- 添加、删除、修改用户端口、密码和连接数限制
- 支持傻瓜式用户添加,小白也可以用
- 自由限制用户端口流量使用及端口网速
- 自动修改防火墙规则
- 自助修改SSR加密方式、协议、混淆等参数
- 自动统计，方便查询每个用户端口的流量使用情况
- 自动安装Libsodium库以支持Chacha20等加密方式
- 支持用户二维码生成(仅开发版可用)
- 支持一键构建ss-panel-V3-mod,前端后端自动对接，无需额外操作（仅开发版可用）
- 傻瓜式的BBR、锐速、LotServer一键构建（有风险，仅开发版可用）
- 可自定义的服务器巡检，故障自动重启服务，确保链接稳定有效
- 可对配置进行备份、还原，迁移服务器只需在新服务器上还原配置，无需重复设置
- 支持IP黑名单功能，可通过端口查询，直接加入黑名单，禁止该IP访问服务器的所有服务
- 允许针对不同用户限制帐号有效期，到期自动删除帐号

## 离线包安装: ##
    wget -q -N --no-check-certificate https://github.com/906296916/SSR-Bash-Python-FunctionClub/raw/master/ShadowsocksrRZ.sh && bash ShadowsocksrR.sh
    
## 安装&更新: ##
    wget -q -N --no-check-certificate https://raw.githubusercontent.com/FunctionClub/SSR-Bash-Python/master/install.sh && bash install.sh

## 自检（没有卵用😝）: ##
    wget -q -N --no-check-certificate https://raw.githubusercontent.com/FunctionClub/SSR-Bash-Python/master/self-check.sh && bash self-check.sh

## 安装bzip2,离线安装失败解决方法[Debian/Ubuntu] : ##
    apt-get install bzip2
    
## 安装bzip2,离线安装失败解决方法[CentOS] : ##
    yum install bzip2

## 卸载: ##
    wget -q -N --no-check-certificate https://raw.githubusercontent.com/FunctionClub/SSR-Bash-Python/master/install.sh && bash install.sh uninstall
 
## --------------------------------------------------------------- ## 

## Centos6/7锐速 ##
**先查看内核版本 安装过程中遇到提示，一路确定即可**

    uname -r
## 结果以 2 开头，例如 2.6.32-696.18.7.el6.x86_64。##
## 这种输出结果说明我们的服务器为 CentOS 6 x64 系统，直接输入以下命令: ##
    wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh && bash appex.sh install '2.6.32-642.el6.x86_64'
    
    
##  结果以 3 开头，例如 3.10.0-693.11.6.el7.x86_64。##
##  这种输出结果说明我们的服务器为 CentOS 7 x64 系统，先输入以下命令: ##
    wget --no-check-certificate -O rskernel.sh https://raw.githubusercontent.com/uxh/shadowsocks_bash/master/rskernel.sh && bash rskernel.sh
##  重启后再输入以下命令: ##
    yum install net-tools -y && wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh && bash appex.sh install
    
##  通用查看锐速命令， 装对了就有信息，没装成功或者没运行成功就没有这个文件 ##
    cat /proc/net/appex/stats

## --------------------------------------------------------------- ## 
        
## 客户端下载 ##
常用平台：[Android](https://github.com/shadowsocksrr/shadowsocksr-latest-bin-backup/raw/master/Shadowsocksr-android-3.4.0.5.apk)、[MacOS](https://github.com/qinyuhang/ShadowsocksX-NG-R/releases/download/1.4.3-R8/ShadowsocksX-NG-R8.dmg)、[Windows](https://github.com/Readour/ShadowsocksR-Csharp/releases/download/4.7.0/ShadowsocksR-4.7.0-win.CONCISE.7z)、[Linux](https://github.com/shadowsocks/shadowsocks-qt5/releases/download/v2.9.0/Shadowsocks-Qt5-x86_64.AppImage)、[OpenWrt/LEDE](https://github.com/bettermanbao/openwrt-shadowsocksR-libev-full/releases)、[iOS](https://github.com/Readour/breakwa11.github.io/raw/master/download/Shadowrocket%202.1.14.ipa)

## --------------------------------------------------------------- ## 

## 宝塔5.9安装 ##
## Centos安装命令： ##
    yum install -y wget && wget -O install.sh http://download.bt.cn/install/install.sh && sh install.sh
## Ubuntu/Deepin安装命令： ##
    wget -O install.sh http://download.bt.cn/install/install-ubuntu.sh && sudo bash install.sh
## Debian安装命令： ##
    wget -O install.sh http://download.bt.cn/install/install-ubuntu.sh && bash install.sh
**面板管理常用命令：https://www.bt.cn/btcode.html**

## --------------------------------------------------------------- ## 

## 花生壳安装 ##
**Ubuntu/Deepin 安装：**

    wget -O http://download.oray.com/peanuthull/linux/phddns_3.0_x86_64.deb  && dpkg -i phddns_3.0_x86_64.deb
**Centos 安装：**

    wget -O http://download.oray.com/peanuthull/linux/phddns-3.0.2.x86_64.rpm && rpm -ivh phddns-3.0.2.x86_64.rpm
