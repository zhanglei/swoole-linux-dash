# linux-tools
linux-tools目录下的是linux性能工具集合，与swoole_vmstat类似

运用swoole友好的实现Linux性能监控工具集合（uptime等）


# Swoole Linux Dash


A simple, low-overhead web dashboard for Linux.



![Swoole Linux Dash screenshot](https://raw.githubusercontent.com/smalleyes/swoole-linux-dash/master/doc/dash1.png)

## 说明
* 一个简单的, 美丽的，基于web的linux监控面板
* 可以运行在传统PHP-FPM环境也可以运行在基于swoole-http-server环境下
* thanks to [https://github.com/afaqurk/linux-dash](https://github.com/afaqurk/linux-dash)

## 安装

### 1. 下载 Swoole Linux Dash

Clone the git repo: 

```linux shell
git clone https://github.com/smalleyes/swoole-linux-dash.git
```

wget the zip file:

```
linux wget https://github.com/smalleyes/swoole-linux-dash/archive/master.zip
```

```
unzip master.zip
```

### 2. 安全
请自行做好安全相关的限制.

## 依赖

* PHP 5.3+
* Swoole 1.7.16
* Linux, OS X and basic Windows support (Thanks to cygwin)

## 安装 Swoole扩展

1. Install from pecl
    
    ```
    pecl install swoole
    ```

2. Install from source

    ```
    sudo apt-get install php5-dev
    git clone https://github.com/swoole/swoole-src.git
    cd swoole-src
    phpize
    ./configure
    make && make install
    ```
## 运行
### 1. 配置NGINX虚拟主机

	1.配置文件位于Doc/dash.conf
	2.复制文件dash.conf到nginx，虚拟主机配置文件目录下（默认为nginx/conf.d目录下）
	3.重启nginx或重新加载nginx配置文件（nginx -s reload）
	3.配置hoshs文件，绑定ip域名对应关系
	4.使用php-cgi或php-fpm确保已正确安装环境再打开浏览器访问绑定的域名.
	5.使用swoole需要启动服务，php web.php再打开浏览器访问绑定的域名
