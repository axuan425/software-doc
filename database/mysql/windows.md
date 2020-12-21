### archive install
1. download
> https://dev.mysql.com/downloads/mysql/5.7.html#downloads

2. unzip & move to basepath

3. create my.ini in basepath
```
[mysql]
# 设置mysql客户端默认字符集
default-character-set=utf8
[mysqld]
# 设置3306端口
port=3306
# 设置mysql的安装目录
basedir=D:\\service\\mysql-5.7.24-winx64
# 设置mysql数据库的数据的存放目录
datadir=D:\\service\\mysql-5.7.24-winx64\\data
# 允许最大连接数
max_connections=200
# 服务端使用的字符集默认为8比特编码的latin1字符集
character-set-server=utf8
# 创建新表时将使用的默认存储引擎
default-storage-engine=INNODB
```

4. install
> open cmd with admin role
> cd ${basepath}/bin
> mysqld --initialize --user=mysql --console
    > when msvcr120.dll error, install the follow file
    > https://www.microsoft.com/zh-CN/download/details.aspx?id=40784
> mysqld --install mysql57
> net start mysql57

5. modify the root password
> mysql -uroot -p'initialize password'
> set password for root@localhost=password("new password")

6. import sql file(must use /, not \\)
> mysql -uroot -p < d:/h.sql

---
