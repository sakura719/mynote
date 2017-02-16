#	mysql
### [菜鸟教程](www.runoob.com)

####*安装*
`sudo apt-get install mysql-server`
`sudo apt-get install mysql-client`

####*启动 |关闭*
`sudo service mysql start | stop`
####*查看进程（检查是否启动）*
`ps -ef|prep mysql`
####*登陆*
`sudo mysql -u root`
```
-u `登陆的用户名`
-P `（大）登陆的端口号` 3306
-p `（小）登陆的密码，若安装时未设置，无需输入`
-D `登陆的哪个数据库`
-h `登陆的主机地址`
```
Ubuntu 16.04 上不能直接用 root 用户登录
`sudo mysql -u root -e "update mysql.user set plugin='mysql_native_password' WHERE User='root'";`

`sudo service mysql restart`

##mysql简单操作

##database
- *创建*
`create database db;`
- *查看*
`show databases;`
- *使用*
`use db;`
- *删除*
`drop database db;`

##table
#### - *创建表*
`create table tb`
```
(id int not null,name varchar(60) not null,score int not null);
```
####*`int` *   *整型*
####*`varchar`*   *字符串*
####*`datatime`*     *时间日期*
#### - *删除*
`drop table tb`

#### - *查看*
`show tables;`

#### - *查看表结构*
`describe tb;` 或者 `show columns in tb;`

#### - *插入数据*
`insert into tb(id,name,score) values(1,'zhang',92) ,(2,'guang',87),(3,'dong',45);`

   *插入多条数据时，直接在后面加逗号，写入插入的数据*

#### - *查看数据*
`select * from tb`   （ 查所有）
`select * from tb where condition`   （单条）
#### - *模糊查询*
`select * from tb where columnname like '%jay'`
```
jay       '代表所知道的'
%jay      '知后不知前'
jay%      '知前不知后'
%jay%     '知中间不知前后'
```
#### - *更新数据*
`update tb set columnName=NewValue [ WHERE condition ]`
#### - *删除数据*
`delete from tb where columnname=''`

#### - *排序*
`select * from tb order by columnname asc/desc` (升/降)

#### - *插入字段*
``

