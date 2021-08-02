# `RabbitMQ`安装

<br>

- ###### [erlang/otp](https://github.com/erlang/otp)环境Github下载地址

- ###### [rabbitmq/rabbitmq-server](https://github.com/rabbitmq/rabbitmq-server)Github下载地址

<br>

<br>

### 一、把下载的文件上传到`Linux`

<br>

![下载的文件](../../../Images/Linux_Install_Images/RabbitMQ_Install_Images/2021-08-02_202334.png)

- 这里我把文件放入了`Linux`的 `/home/mytest/`目录文件夹下

```shell
//进入mytest目录文件夹
cd /home/mytest/
```

<br>

<br>

<br>

### 二、解压&安装`Erlang`

- 先解压`otp_src_24.0.5.tar.gz`文件到`/usr/local/`目录文件夹下

```shell
tar -zxvf otp_src_24.0.5.tar.gz -C /usr/local/
```

<br>

- 安装`RabbitMQ`之前必须要先安装所需要的依赖包可以使用下面的一次性安装命令

```shell
yum install gcc glibc-devel make ncurses-devel openssl-devel xmlto -y
```

<br>

