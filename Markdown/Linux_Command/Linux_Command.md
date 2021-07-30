# Linux常用命令

<br>

`新建文件夹`

```shell
mkdir	文件名
```

`新建一个名为test的文件夹在home下`

```shell
mkdir /home/test
```

<br>

`新建文本`

```
vi	文件名
```

`在home下新建一个test.sh脚本`

```shell
vi /home/test.sh
```



3.删除文件或文件夹

1、删除home目录下的test目录

 rm /home/test



2、这种不带参数的删除方法经常会提示无法删除，因为权限不够。

 rm -r /home/test



3、-r是递归的删除参数表中的目录及其子目录。 目录将被清空并且删除。 当删除目录包含的具有写保护的文件时用户通常是被提示的。

rm -rf /home/test



-4、f是不提示用户，删除目录下的所有文件。请注意检查路径，输成别的目录就悲剧了。

 rm -ir /home/test



5、-i是交互模式。使用这个选项，rm命令在删除任何文件前提示用户确认。



4.移动文件或文件夹

mv [options] 源文件或目录 目标文件或目录


