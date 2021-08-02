# `RabbitMQ`安装

<br>

- ###### [erlang/otp](https://github.com/erlang/otp)环境Github下载地址

- ###### [rabbitmq/rabbitmq-server](https://github.com/rabbitmq/rabbitmq-server)Github下载地址

<br>

<br>

### 一、把下载的文件上传到`Linux`

<br>

![下载的文件](https://github.com/Dashan-37/Notes/raw/master/Images/Linux_Install_Images/RabbitMQ_Install_Images/2021-08-02_202334.png)

- 这里我把文件上传到`Linux`的 `/home/mytest/`目录文件夹下`该步骤省略`
- 进入`mytest`目录文件夹

```shell
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

- 进入到`/usr/local/otp_src_24.0.5/`目录文件夹下

```shell
cd /usr/local/otp_src_24.0.5/
```

<br>

- 配置`erlang`的安装信息

```shell
./configure --prefix=/usr/local/erlang --without-javac
```

<br>

- 编译并安装

```shell
make && make install
```

<br>

- 进入`/usr/local/erlang/` `erlang`安装目录文件夹下

```shell
cd /usr/local/erlang/
```

<br>

- 配置环境变量

```shell
vim /etc/profile
```

<br>

- 将这些配置填写到profile文件的最后
- erlang安装目录`/usr/local/erlang`

```shell
ERL_HOME=/usr/local/erlang
PATH=$ERL_HOME/bin:$PATH
export ERL_HOME PATH
```

<br>

- 保存退出

```
:wq
```

<br>

- 启动环境变量配置文件

```shell
source /etc/profile
```

<br>

- 查看安装版本

```
erl -version
```

<br>

- 如果出现`Erlang (SMP,ASYNC_THREADS) (BEAM) emulator version 12.0.3`则表明安装成功

